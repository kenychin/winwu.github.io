---
layout: post
category : Windows-8-app
date: 2013-09-20 12:00:00
title : Day5  Windows API  For Windows App（一） WinRT
tagline: "HTML5 X JavaScript 開發 Windows 8 Apps"
tags : [windows 8 App]
---
{% include JB/setup %}


* 這個啊，其實還重要的，嚴格來講其實是因為後面後開始介紹怎麼使用 windows UI 的組件，主要是為了這個目的，用法你會很常看到我們使用 『 `WinJS.UI.XXXXX` 』做些事情。
* 比方說你要做可以做評分的星星，那麼你就會用到 `WinJS.UI.Rating`;
* 比方說你要做搜尋框，那麼就會用到 `WinJS.UI.SearchBox`。

---

###Windows 主要會提供兩種 API
* WinRT : Windows Runtime
* WinJS : Windows Library for JavaScript
* 今天介紹 WinRT


---

###Windows Runtime：
* 有的人會直接稱他為 『WinRT』或 windows 執行庫。
另外也有人認為它是一個 Framework 而不覺得他是 API，這個...跟一些.NET的歷史有關，因為我不了解這段過去，有興趣的朋友可以自行搜尋多了解。

* Windows 8 App 雖然能夠使用各種不同語言實作，但不論是哪種語言，實作出來的結果都必須透過(訪問, Access)一個叫做 Windows Runtime 的 API（感覺像是很多 API 的集合），講白一點就是它是建構 windows App 的一個 API，我自己是覺得他感覺是比較偏底層的，是用來協助跟作業系統（OS，在這裡所指的就是 Windows 8 ）溝通的作用。

* 另外，WinRT 裡面的 API 定義是遵循 ECMA 335 的標準。

### WinRT 有哪些 API 呢？

* (WinRT 的 API 其 Namespace 都是以 Windows 為首，還蠻好記的。)好多，但很難懂...，可能是我還用不到吧，以下列到的都是：
	* Windows.ApplicationModel (讓 app 取得 package 的資訊。)
	* Windows.Foundation (啓用一些功能，像是非同步操作的管理， 取得已儲存的屬性，圖片或是 URI。)
	* Windows.Management
	* Windows.Data
	* Windows.Devices (跟一些裝置有關，像相機, 羅盤, GPS等等。)
	* Windows.System
	* Windows.UI (WinRT 最大的 namespace，可以在這裡找到很多啓動觸控的UI元件)
	* Windows.Globalization
	* Windows.Graphics
	* Windows.Media
 	* Windows.Networking
	* Windows.Security
	* Windows.Storage
	* Windows.Web


* WinRT 我覺得太抽象了，感覺我應該要到一定的 level 才能理解啊～
下一篇會提到另外一個 API，`Windows Library for JavaScript(WinJS)`，這個稍微好理解一點。

---

###參考資源：
* [Windows API reference for Windows Store apps](http://msdn.microsoft.com/en-US/library/windows/apps/br211377)
* [Windows Runtime(WinRT) 揭秘](http://www.cnblogs.com/shanyou/archive/2011/09/17/WinRT.html)
* [wikipedia-Windows Runtime](http://en.wikipedia.org/wiki/Windows_Runtime)
* [A Brief Introduction to WinJS](http://dev.bennage.com/blog/2012/08/01/a-brief-introduction-to-winjs/)
* [Windows API reference for Windows Store apps](http://msdn.microsoft.com/en-us/library/windows/apps/br211377.aspx)
* [Windows 8 Application Development with HTML5 For Dummies](http://www.dummies.com/how-to/content/windows-8-application-development-with-html5-for-d.html) 
* [Promises/A](http://wiki.commonjs.org/wiki/Promises/A)
* [問八系列 與 Windows Runtime Library 是麻吉的好朋友：JavaScript + WinJS](http://www.dotblogs.com.tw/regionbbs/archive/2011/09/19/javascript.and.winjs.in.windows.8.aspx)


---

* 今日進度結束。
* 如有任何問題，歡迎留言。雖然我不一定會 :P，但盡可能找到 reference 或解答。
