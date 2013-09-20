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
* 有的人會直接稱他為 `WinJS`。
* 這個 API 跟 Windows Runtime 是不一樣的,他是純 JavaScript。
* 這類的 API 都是提供一些 windows 8 app style 的元件。
* 不過要注意的是,如果你要使用這個 API,你一定要載入 `base.js` ,然後再載入 `ui.js`, 這部分 先知道這些觀念就好,通常當我們建立空白的 App 專案時,其會幫你產生 `default.html` 這個檔案,裡面已經幫你寫好了,像這樣:

	```<script href="//Microsoft.WinJS.1.0/js/base.js"></script>```
	
	```<script href="//Microsoft.WinJS.1.0/js/ui.js"></script>```

		
* WinJS 可以讓你自己擴充功能,它可以讓你自己定義命名空間。WinJS 包含了以下幾種很有幫助的事:
	* 實踐 CommonJS Promises/A
	* UI組件
	* DOM utilities
	* 導航 and xhr

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
