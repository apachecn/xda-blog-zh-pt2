# Weather App by Example 教授 JSON、HTTP 和 API 的使用

> 原文：<https://www.xda-developers.com/weather-app-by-example-teaches-json-http-and-api-use/>

刚刚入门的开发人员可以通过阅读更有经验的程序员编写的代码来跨越学习曲线。如果你能读懂每个代码块的解释，就像这篇天气应用教程一样，那就更有用了。Francesco Angola 也写了 Httpclient 使用指南[，他在解释如何使用网站 API、解析 JSON 字符串并将结果呈现给用户方面做了大量工作。](http://www.xda-developers.com/android/httpclient-tutorial-to-upload-and-download-with-your-app/)

Francesco 从探索从[开放天气地图 API](http://openweathermap.org/api) 获得的数据开始。不要被那个网页标题迷惑了。这里的目标是收集当前天气状况的文本数据，而不是显示在屏幕地图上。在浏览器中输入 URL 会返回一个 JSON 字符串，他使用该字符串的格式在 JSONObject 和 JSONArray 类的帮助下创建一个解析器方法。我认为这是指南的核心。解析器为如何存储数据对象设计了一个路线图。在使用 JSON 格式时，这种技术很容易适应。从这里开始，他使用 HttpClient 获取提供给解析器的字符串。该指南最后创建了一个在屏幕上显示天气状况的基本活动。

去他的博客看完整的教程。

*【Via[Reddit](http://www.reddit.com/r/androiddev/comments/1erp5l/build_real_weather_app_json_http_and/)*