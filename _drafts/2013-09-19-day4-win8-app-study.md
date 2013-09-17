---
layout: post
category : Windows-8-app
title : Day3 Programming Windows 8 Apps with HTML CSS and JavaScript ~ ch01讀書筆記
date: 2013-09-18 16:00:00
tagline: "HTML5 X JavaScript 開發 Windows 8 Apps"
tags : [windows 8 App]
---
{% include JB/setup %}

### 書目 : Programming Windows 8 Apps with HTML CSS and JavaScript
### 章節 Chapter 1 

* 以下僅是個人對書目內容的理解，如果錯誤煩請糾正，謝謝:)
 
---

* windows 8 的團隊做了一個系統的API，可以讓很多不同的程式語言去使用，`包含JavaScript`，簡單來說可以用各種不同語言，開發最後長得差不多的東西，看你會哪種。那個這個 API ，就是鼎鼎有名的`Windows Runtime API`，如果你看很多文件，有的人會簡稱 `WinRT`，也就是指`Windows Runtime API`。

* WinRT 這個 API，做的事情包含了這個 object 怎麼被創造，事件, error, expections 的處理, 處理非同步, 如何保持畫面的順暢, 滑動的效果, 方法,屬性等等。

* 你所開發的 Windows 8 App，上架的地點絕對不是菜市場，更不是你家，唯一的上架地點就是 Windows App Store(恩…要註冊哦...)，Visual Studio 有個很方便的功能可以讓你直接打包 (package) 你所開發的App，就是 `Store/Upload App Package` 指令。

* 當你使用 visual studio 開發 win8 app 時，每個專案應該可以說成是一個 package，這個 package 本身是一個附檔名是 `.appx` 的檔案，這個檔案包含你的程式碼，你的其他資料的來源， librares，以及 `manifest`。

* `manifest` 是一個神秘檔案，ＸＤ，依照我的理解，它會自己產生，不太可能是手動建的，它記載著你當下那個 app 的基本資料，像是 App 的名字，logo是哪幾張啊～，之類的。

* 中間好幾段都在講 windows store 市集，這個比較沒什麼好寫的，先跳過。

---

#### 什麼是 Windows Library for JavaScript?
* 也被稱為`WinJS`
* html, css, JavaScript 其實是在 App 執行的時候，被載入（html）, 被編譯(javascript), 被 render（css） 出來的，最後經過 WinJS ，很多 App 預設的行為，樣式也會一起幫你做出來。也就是說 WinJS 提供很多現成的效果可以直接使用，你不需要為了做出符合 windows 8 app 的 User Experience (比方說一些動畫的效果, 事件跟行為) 的效果而自己重造輪子。

---


今日進度結束，請等待下一篇。

本篇同時轉載於 [it邦幫忙](http://ithelp.ithome.com.tw/question/10126693)。

如有任何問題，歡迎留言。雖然我不一定會 :P，但盡可能找到 reference 或解答。
