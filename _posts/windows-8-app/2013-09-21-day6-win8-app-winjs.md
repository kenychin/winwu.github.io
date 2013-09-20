---
layout: post
category : Windows-8-app
date: 2013-09-21 12:00:00
title : Day6  Windows API  For Windows App（二） WinJS
tagline: "HTML5 X JavaScript 開發 Windows 8 Apps"
tags : [windows 8 App]
---
{% include JB/setup %}

繼上一篇介紹 WinRT ,接下來要聊 WinJS。
###Windows Library for JavaScript:





	```<script href="//Microsoft.WinJS.1.0/js/base.js"></script>```
	
	```<script href="//Microsoft.WinJS.1.0/js/ui.js"></script>```

		






---

###WinJS 有哪些 API 呢? 舉例來說:
    
* WinJS.Application

* WinJS.Binding

* WinJS.Class

* WinJS.Namespace

* WinJS.Navigation

* WinJS.Resources
* WinJS.UI (初學時會最常用到這個)
* WinJS.UI.Rating
* WinJS.UI.AppBar
* WinJS.UI.FlipView
* WinJS.Utilities

<p>最後要順帶一提的是,這兩個 API( WinRT 跟 WinJS ) 是 only for Windows Store App,也就是說只能用在開發 windows 8 app 應用程式市集的 App,並沒有支援瀏覽器,也就是你直接點首頁 default.html 是可以用瀏覽器開，可是不會是你想要的樣子。</p>

---

## WinRT v.s WinJS
* 可以把 WinRT (Windows Runtime) 想像成是一個運行的平台。而 WinJS 可以跑在 WinRT(Windows Runtime) 上。


今日進度結束。

如有任何問題，歡迎留言。雖然我不一定會 :P，但盡可能找到 reference 或解答。