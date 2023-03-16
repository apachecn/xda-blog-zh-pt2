# Google Pay for India 准备增加 2020 邮票奖励、一次性授权等等！

> 原文：<https://www.xda-developers.com/google-pay-tez-india-2020-stamp-rewards-one-time-mandates-stories-merchants/>

**更新 2(美国东部时间 2019 年 12 月 23 日凌晨 3 点 12 分):** 2020 年邮票奖励现已在印度 Google Pay (Tez)上推出。

**更新(美国东部时间 2019 年 12 月 18 日凌晨 1:40):**我们现在有一些即将推出的 2020 年邮票和令牌化卡片的截图。滚动到底部了解更多信息。这篇发表于 2019 年 12 月 12 日的文章被保存如下。

[Google Pay](https://www.xda-developers.com/google-pay-tests-safetynet-status-protecting-online-purchases-pin/) 是谷歌的统一支付平台，但该公司也有一个名称相同但功能不同的应用程序供印度用户使用。这个[独有的 Google Pay 是以前](https://www.xda-developers.com/google-for-india-event-announcements/) [Google Tez](https://www.xda-developers.com/google-tez-7-5-million-users-india/) 的更名，更名后，该应用程序继续增加[更多功能。我们上次发现 Google Pay (Tez)准备为其印度用户增加黄金礼品选项。现在，该应用程序正准备为 2020 年带来邮票奖励、一次性授权和商户故事。](https://www.xda-developers.com/google-pay-tez-india-material-theme-redesign/)

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

Google Pay (Tez) 49.0.003_RC05 包含新的字符串，表明 Google 正在开发一些新功能。

## Google Pay - 2020 邮票奖励

在最近的印度节日期间，谷歌通过其排灯节邮票奖励活动获得了金牌。Google Pay 向用户提供了收集 5 枚排灯节主题邮票的任务，承诺保证支付₹251(3.5 美元)，并有机会赢得₹1,00,000 大奖(1400 美元)。

其中一些邮票可以通过扫描你周围的排灯节物品来获得，而其他一些邮票，如 Rangoli 和 Flower，可以通过在应用程序中支付账单和其他商业交易来获得。你也可以向其他用户赠送邮票，并向他们索要一张。谷歌还在最后添加了一个排行榜，本质上使整个体验成为一场集邮游戏。这场运动的最终结果是，它真的受到了印度城市观众的欢迎，并因积极的原因而像病毒一样传播开来，因为用户开玩笑地争相收集所有的邮票，赢得他们确定的奖品，并参加大奖。谷歌没有公布这场活动的任何指标，但从社交媒体和我周围的观察来看，这场活动确实将 Google Pay 作为首选支付方式，即使只是在活动期间。

现在，谷歌的目标是在新的一年复制同样的成功，因为字符串表明 2020 年类似的活动正在进行中。以下是 Google Pay(Tez)v 49 新增的字符串:

```
 <string name="adcatcher_ui_listening_description_1_with_youtube_link_2020">"Catch an ad to collect a reward! Just stay on this page when you're listening to a Google Pay ad on TV or Google India's %1$s playlist."</string>
<string name="adcatcher_ui_listening_description_2_2020">"Open the Youtube playlist on a different device to listen to it now. The microphone only listens on this On-Air page, and audio never leaves your device."</string>
<string name="adcatcher_ui_dialog_reward_daily_limit_action">Got it</string>
<string name="adcatcher_ui_dialog_reward_daily_limit_title">"You've reached the daily limit"</string>
<string name="adcatcher_ui_dialog_reward_general_error_action">Try again</string>
<string name="adcatcher_ui_dialog_reward_general_error_description">Try again in a short while.</string>
<string name="adcatcher_ui_dialog_reward_general_error_title">Something went wrong</string>
<string name="adcatcher_ui_dialog_reward_success_action">Keep playing</string>
<string name="adcatcher_ui_dialog_reward_success_description">"Congrats, you've collected a 2020 stamp!"</string>
<string name="adcatcher_ui_dialog_reward_success_title">1 %1$s</string>
<string name="adcatcher_ui_dialog_reward_timeout_action">Try again</string>
<string name="adcatcher_ui_dialog_reward_timeout_description">"We couldn't find the number 2020 with the audio scanner. Bring your phone closer or try with a different ad."</string>
<string name="adcatcher_ui_dialog_reward_timeout_title">Our scanner timed out</string>
<string name="adcatcher_ui_listening_toast_retry_2020">"Can't hear any ads. Move your phone closer to the speaker or try a different ad."</string> 
```

虽然排灯节邮票活动包括用手机的摄像头扫描 diyas 等排灯节物品，但 2020 年的活动可能会涉及摄像头和麦克风，作为赚取邮票的两种手段。上面的字符串表明，用户将不得不利用手机的麦克风来收听电视上的谷歌支付广告或谷歌印度的 YouTube 播放列表。音频扫描仪将尝试在广告音频中提取数字“2020 ”,并奖励用户一枚 2020 主题邮票。

一些旧字符串的描述也发生了变化:

*   *<string name = " Diwali _ scandi Wali _ hint _ on _ what _ to _ Scan ">扫描一个排灯节物品收集一枚邮票< /string >* **改为***<string name = " Diwali _ scandi Wali _ hint _ on _ what _ to _ Scan ">扫描你附近任何地方的数字“2020”收集一枚邮票！</字符串>*
*   *<string name = " social _ Diwali _ scan _ success _ description ">"恭喜你，你已经收集了一枚排灯节邮票！继续玩，完成你的一套。”< /string >* **改为***<string name = " social _ Diwali _ scan _ success _ description ">“恭喜你，你已经收集了一枚 2020 年邮票！”</字符串>*
*   *<string name = " social _ Diwali _ scan _ time out _ description ">我们无法检测到任何排灯节项目。请将您的扫描仪移近一点，或者尝试不同的项目。< /string >* **改为***<string name = " social _ Diwali _ scan _ time out _ description ">“我们用 AR 扫描仪找不到 2020 这个数字。请将您的手机拉近一些，或者尝试使用不同的图像。”</字符串>*

这些表明，简单地扫描数字 2020 也将为您赢得一枚邮票，尽管我们认为有些邮票将无法通过这种媒体获得，就像 Rangoli 和 Flower 在之前的活动中无法通过扫描获得一样。

距离 2020 年还有半个月的时间，所以我们必须等待听到更多关于奖励和其他活动细节的消息。

## 商人的故事

这个新版本的 Google Pay 还准备允许商家添加故事。

```
 <string name="merchantstories_content_description">%1$s story button</string>
<string name="merchantstories_more_stories_title">See all</string>
<string name="merchantstories_stories_title">Highlights</string> 
```

为什么我们需要 Google Pay 中的故事？我们只能推测。谷歌最近确实在 Google Photos 中添加了[私人信息，那么为什么不在 Google Pay 中也添加一些故事呢？我们还做出了一个有根据的猜测，在这种情况下，“故事”指的是社交媒体网站在其平台上整合的临时照片和视频亮点。](https://www.xda-developers.com/google-photos-adds-private-messaging-share-photos/)

## 一次性任务

一次性授权是 [UPI 2.0 功能推出](https://www.npci.org.in/sites/default/files/circular/Rollout%20of%20UPI%202.0.pdf)的一部分。利用这一功能，用户可以预授权交易并冻结其账户中的资金，以便以后将其记入借方。这种冻结可以确保您的帐户中有足够的资金，直到交易需要执行，您可以继续赚取利息，并允许自动安排和执行交易。

Google Pay (Tez) v49 包含几个新字符串和几个用于一次性授权的旧字符串:

新字符串

```
 <string name="india_mandates_preferences_title">One-Time Mandates</string>
<string name="india_mandates_mandateamount_error_max_amount_text">Maximum amount %s</string>
<string name="india_mandates_mandateamount_error_min_amount_text">Minimum amount %s</string>
<string name="india_mandates_mandateamount_input_hint">Amount</string> 
```

旧字符串:

```
 <string name="india_mandates_action_paying_to">Paying to</string>
<string name="india_mandates_action_sending">Sending request…</string>
<string name="india_mandates_amount_paid_label">Amount paid</string>
<string name="india_mandates_call_bank_message">Try calling your bank.</string>
<string name="india_mandates_cannot_reach_bank">"We can't reach your contact's bank. Please try again later."</string>
<string name="india_mandates_category_title">Mandates</string>
<string name="india_mandates_content_source_failure">Could not get mandates from server</string>
<string name="india_mandates_end_date_label">End date</string>
<string name="india_mandates_execution_date_label">Execution date</string>
<string name="india_mandates_incorrect_pin_message">To continue, please raise a new mandate.</string>
<string name="india_mandates_incorrect_pin_title">Incorrect UPI PIN</string>
<string name="india_mandates_insufficient_funds_title">Insufficient funds</string>
<string name="india_mandates_mandate_details_label">Mandate details</string>
<string name="india_mandates_mandate_name_label">Mandate name</string>
<string name="india_mandates_notes_label">Notes/description</string>
<string name="india_mandates_original_amount_header">Original amount</string>
<string name="india_mandates_original_end_date_header">Original end date</string>
<string name="india_mandates_payment_disclaimer">Payments may take up to 3 working days to be reflected in your account</string>
<string name="india_mandates_purpose_code_label">Purpose code</string>
<string name="india_mandates_request_failed">Request failed</string>
<string name="india_mandates_start_date_label">Start date</string>
<string name="india_mandates_status_approve_by">Confirm by %1$s</string>
<string name="india_mandates_status_approve_within">Confirm within %1$s</string>
<string name="india_mandates_status_countdown">%1$shr %2$smin</string>
<string name="india_mandates_status_declined_on">Mandate declined on %1$s</string>
<string name="india_mandates_status_executed_on">Mandate executed on %1$s</string>
<string name="india_mandates_status_expired_on">Mandate expired on %1$s</string>
<string name="india_mandates_status_label">Status</string>
<string name="india_mandates_status_refunded_on">Mandate refunded on %1$s</string>
<string name="india_mandates_transaction_details_label">Transaction details</string>
<string name="india_mandates_try_again_title">Try again</string>
<string name="india_mandates_unique_number_label">Unique mandate number</string>
<string name="india_mandates_updated_amount_header">Updated amount</string>
<string name="india_mandates_updated_end_date_header">Updated end date</string>
<string name="india_mandates_upi_credentials_challenge_permission_required_error_description">%1$s needs your phone permissions to ensure that the SIM card in your phone matches with the registered mobile number.</string>
<string name="india_mandates_upi_restore_primer_description">You need to reactivate the following bank account:</string>
<string name="mandates_browsing_details_announce_content_description">Details of mandate</string>
<string name="mandates_browsing_list_announce_content_description">List of mandates</string> 
```

因为我们发现了新旧字符串的组合，所以我们不确定该功能是否是新的，对于某些用户来说是否已经存在。主偏好标题是刚刚添加的，所以我们倾向于认为该功能尚未上线。

* * *

## 更新:2020 年邮票和令牌化信用卡登录页面的截图

Twitter 用户 Rohan Bathla 已经成功启用了令牌化信用卡功能的初始登录页面以及 2020 年邮票。然而，点击这些还没有引起任何反应。

令牌化卡支持早在 2019 年 9 月的谷歌印度活动上就已宣布。该功能的字符串在几个版本的应用程序中就已经存在，但由于该功能已经公布，这些并不是特别有趣。然而，这些浮出水面表明，该功能最终准备推出，我们可以期待很快听到更多关于它的消息。

用户还设法为即将到来的 2020 邮票功能打开了功能重定向窗口。

* * *

## 更新 2: 2020 邮票现已上线！

正如预测的那样，2020 邮票及其奖励现已在印度用户的 Google Pay (Tez)中上线。

谷歌声称，除了太妃糖、DJ 和披萨之外的邮票将被可变地分发。幸运的是，这三个戳记在指定动作(账单支付、移动充值和新用户邀请)的第一个实例中得到保证，这是一个受欢迎的变化，因为上次这也是一次抽奖。这次的奖励范围从完成所有蛋糕层后支付₹202(2.8 美元)-₹2020(28.3 美元)，以及完成每一层的奖金奖励，包括代金券、刮刮卡和幸运抽奖票。2020 年邮票节/游戏将持续到 2019 年 12 月 31 日，但我们预计谷歌将再延长一周。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*