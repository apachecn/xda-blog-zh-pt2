# 我如何破解琐事裂缝

> 原文：<https://www.xda-developers.com/how-i-cracked-trivia-crack/>

琐事裂纹是一个非常受欢迎的网络和移动平台的游戏，有点模仿琐碎的追求。这是社交游戏的最新热潮，允许用户与他们的朋友和陌生人竞争回答一系列类别的问题。尽管我对游戏从来都不感兴趣，但我妻子最近却成了《琐事破解》的超级粉丝。看了她玩了一会儿，我决定下载下来，仔细看看是怎么实现的。

我开始是在使用 Android 应用程序时监控网络上发出的 web API 请求。很快，我在游戏运行过程中注意到了一些有趣的事情。似乎在用户开始转动“类别”转盘之前，应用程序就已经收到了来自琐事破解服务器的类别、问题和答案。

下面是应用程序在显示此屏幕之前获取的示例响应:

```
{

【id】:2747994099，

“对手”:{

【id】:0，

" alerts_count": 0，

"用户名":" smartplay(tm)"

 },

“游戏 _ 状态”:“待定 _ 批准”，

《语》:“恩”，

"已创建": "美国东部时间 2015 年 3 月 23 日 08 时 58 分 29 秒"，

" last _ turn ":" 03/23/2015 08:58:29 EST "，

“类型”:“正常”，

"失效日期":" 2015 年 6 月 3 日 08:58:29 东部"，

“轮到我了”:真的，

"统计数据":{

"玩家 _ 一个 _ 统计":{

"类别 _ 问题":[

 {

「类别」:「地理」，

【正确】:1，

“不正确”:0，

“最差”:错误

 }

 ],

「正确 _ 答案」:1，

“不正确的答案”:0，

“挑战 _ 胜利”:0，

【问题 _ 已回答】:1，

“克朗 _ 韩元”:0

 },

"玩家二统计":{

「正确答案」:0，

“不正确的答案”:0，

“挑战 _ 胜利”:0，

“问题 _ 已回答”:0，

“克朗 _ 韩元”:0

 }

 },

" dujemma type ":false，

正常类型:true，

" spins_data": {

"旋转":[

 {

“类型”:“正常”，

"问题":[

 {

"问题":{

【id】:14996887，

「品类」:「运动」，

“text”:“谁是第一个在奥运会上获得满分 10 分的女子体操运动员？”,

"答案":[

"Nadia Comaneci",

“莫慧兰”，

“塔季扬娜·古楚”，

爱格妮丝

 ],

"作者":{

【id】:71534267，

【姓名】:“弗洛伦蒂娜·尤内拉·加利亚诺”，

“用户名”:“florentina.gagliano”，

" facebook_id": "100000030456122 "，

" Facebook _ name ":" florent ina Ionela Gagliano "，

“fb_show_picture”:真，

" fb_show_name": true

 },

「正确 _ 答案」:0，

" media_type ":"正常"

 },

"通电问题":{

【id】:8534934，

「品类」:「运动」，

" text ":"在篮球中，把它从玻璃上吻下来"是什么意思？",

"答案":[

“两罚全中”，

“放过某人的后背”，

“运球越过两个人”，

"从篮板上击出一球"

 ],

"作者":{

【id】:41439403，

【名称】:“tsan.819”，

"用户名":" tsan.819 "，

“fb_show_picture”:假，

" fb_show_name": false

 },

「正确 _ 答案」:3，

" media_type ":"正常"

 }

 }

 ]

 }

 ]

 },

" available _ crown ":[

“科学”，

“艺术”，

“历史”，

“娱乐”，

“运动”，

“地理”

 ],

“我的 _ 玩家 _ 号码”:1，

“available _ extra _ shots”:1、

"玩家一":{

【收费】:1 元

 },

"玩家二":{

【收费】:0

 },

" round_number": 1，

" sub _ status ":" P1 _ 玩 _ 第一回合"，

" previous _ sub _ status ":" P1 _ 等待 _ 第一次 _ 转弯"，

“is_random”:真，

“未读消息”:0，

“状态 _ 版本”:1，

“新 _ 成绩”:假，

"我的级别数据":{

【等级】:1、

【要点】:1、

【进步】:33，

《goal _ points》:3、

“level_up”:假

 }

}
```

请注意，类别、问题、答案选项和正确答案都包含在回复中。这意味着当在应用程序中被要求作弊时，很容易识别答案。虽然对游戏使用来说不太道德或公平，但我认为这将是一项有趣的研究。

我最初的计划是对 Android 应用程序进行逆向工程，并为用户提供一个答案的 [Toast](http://developer.android.com/guide/topics/ui/notifiers/toasts.html) 通知。我从[反编译应用](http://www.decompileandroid.com/)和审查源代码开始。我使用 grep 在源代码中搜索一些关键字，希望这些关键字能帮助我追踪问答活动。在搜索一些可能的结果时，有几行引起了我的注意。

```
 v.setText(p);

字符串 s1 =

if(com . eter max . tools . f . a . a()& & h . a(" ANSWERS _ CHEAT "，true))

 {

s1 = (new StringBuilder())。追加("(")。append(r . getcorrectsanswer())。追加(")")。toString()；

 }

B.setText((new StringBuilder())。append(r.getText())。追加(s1)。toString())；

a . setcontentdescription(r . gettext())；

甲(乙)；

u . set visibility(0)；

c . start animation(com . eter max . preguntados . ui . a . c . b())；

x . set image resource(com . eter max . preguntados . ui . game . duel mode . h . a(m))。a(g，r . get category())；

LayoutInflater layoutinflater;

列表列表；

如果(l！= null && l == GameType。决斗 _ 游戏)

 {

y . set visibility(0)；

y.setText(c(c.x()。h()))；

}否则

 {

y . set visibility(8)；

 }

h . set enabled(false)；

layoutinflater = getLayoutInflater(getArguments());

d . a(e . d)；

list = r . getanswers()；
```

遵循代码，“ANSWERS_CHEAT”暗指游戏中隐藏的作弊模式。我决定找出它是如何工作的，而不是重新发明轮子。使用 grep，我找到了对“ANSWERS _ CHEAT”字符串 的所有引用，并很快 发现了对主仪表板活动上隐藏菜单的引用。

```
 public boolean onOptionsItemSelected(MenuItem menuitem)

 {

if(com . eter max . tools . f . a . a()& & menuitem . getitemid()= = com . eter max . I . cheat)

 {

if (j.a("ANSWERS_CHEAT "，真))

 {

j.b("ANSWERS_CHEAT "，假)；

menuitem.setTitle("启用答案作弊")；

返回 true

}否则

 {

j.b("ANSWERS_CHEAT "，真)；

menuitem.setTitle("禁用答案作弊")；

返回 true

 }

}否则

 {

返回 super . onoptionsitems elected(menuitem)；

 }

 }
```

这段代码似乎可以处理作弊模式选项的设置，但我仍然无法访问菜单本身。在同一活动中，我回顾了下面的 OnCreateOptionsMenu 方法:

```
 public boolean onCreateOptionsMenu(Menu menu)

 {

if (com.etermax.tools.f.a.a())

 {

getMenuInflater()。inflate(com . eter max . l . preguntados _ debug _ menu，menu)；

返回 true

}否则

 {

return super . oncreateoptionsmenu(菜单)；

 }

 }
```

大多数作弊模式功能，包括隐藏菜单，看起来都依赖于com . etermax . tools . f . a . a()的返回值。该类的代码如下:

```
public class a

{

私有静态布尔 a；

私有静态字符串

公共静态 void a(application info application info)

 {

a =假；

 }

公共静态 void a(字符串 s)

 {

b = s；

 }

公共静态布尔 a()

 {

返回 a；

 }

公共静态字符串 b()

 {

返回 b；

 }

公共静态布尔 c()

 {

回归 b！= null

 }

}
```

这似乎是我一直在寻找的决策点。改变赋值 a =假；到真应该已经启用了隐藏菜单。我打开了类的 smali 表示，找到了布尔成员的赋值。

```
# direct methods

。方法 public static a(land roid/content/pm/application info；)V

。本地人 1

。序言

。第 29 行

常数/4 v0，0x0

sput-boolean v0，Lcom/eter max/tools/f/a；->答:Z

。第 30 行

返回-无效

。结束方法
```

我将第 29 行(上面的代码片段第 7 行)改为 const/4 v0，1 ，将值设置为 true。然后我重新编译并安装了这个应用程序。菜单按钮成功地暴露了下面隐藏的选项:

“答案作弊”现在似乎默认启用，所以我开始了一个新的游戏来测试。不出所料，游戏现在在问题后面附加了一个数字，表示正确答案的从零开始的索引。

点击下载 APK 补丁[。请注意，这仅用于研究目的；我不对任何不道德的游戏负责！](http://www.mediafire.com/download/0e1mbz6rchavc9r/Trivia_Crack_com.etermax.preguntados.lite_2.0.1_71.apk)

**编辑:** [APK 镜报](http://www.filedropper.com/triviacrackcometermaxpreguntadoslite20171)

这应该是一个很好的例子，说明客户端应用程序的隐私无法得到保证，开发人员应该小心他们编译的版本中包含的内容。