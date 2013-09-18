---
layout: post
category : Windows-8-app
title : Day4 Programming Windows 8 Apps with HTML CSS and JavaScript ~ ch01讀書筆記

tagline: "HTML5 X JavaScript 開發 Windows 8 Apps"
tags : [windows 8 App]
---
{% include JB/setup %}

### 書目 :<br/> Programming Windows 8 Apps with HTML CSS and JavaScript


---

### 本次章節： Chapter 1  

---

* 書本連結 [Free ebook: Programming Windows 8 Apps with HTML, CSS, and JavaScript](http://blogs.msdn.com/b/microsoft_press/archive/2012/10/29/free-ebook-programming-windows-8-apps-with-html-css-and-javascript.aspx)

##### 以下僅是個人對書目內容的理解，如果錯誤煩請糾正，謝謝。
* windows 8 的團隊做了一個系統的API，可以讓很多不同的程式語言去使用，`包含JavaScript`，簡單來說可以用各種不同語言，開發最後長得差不多的東西，看你會哪種。那個這個 API ，就是鼎鼎有名的`Windows Runtime API`，如果你看很多文件，有的人會簡稱 `WinRT`，也就是指`Windows Runtime API`。

* WinRT 這個 API，做的事情包含了這個 object 怎麼被創造，事件, error, expections 的處理, 處理非同步, 如何保持畫面的順暢, 滑動的效果, 方法,屬性等等。

* 你所開發的 Windows 8 App，上架的地點絕對不是菜市場，更不是你家，唯一的上架地點就是 Windows App Store (恩…要註冊哦...)，Visual Studio 有個很方便的功能可以讓你直接打包 (package) 你所開發的App，就是 `Store/Upload App Package` 指令。

* 當你使用 visual studio 開發 win8 app 時，每個專案應該可以說成是一個 package，這個 package 本身是一個附檔名是 `.appx` 的檔案，這個檔案包含你的程式碼，你的其他資料的來源， librares，以及 `manifest`。

* `manifest` 是一個神秘檔案，ＸＤ，依照我的理解，它會自己產生，不太可能是手動建的，它記載著你當下那個 app 的基本資料，像是 App 的名字，logo是哪幾張啊～，之類的。

* 中間好幾段都在講 windows store 市集，這個比較沒什麼好寫的，先跳過。

---

### 什麼是 Windows Library for JavaScript?

* 也被稱為`WinJS`
* html, css, JavaScript 其實是在 App 執行的時候，被載入（html）, 被編譯 (javascript), 被 render (css) 出來的，最後經過 WinJS ，很多 App 預設的行為，樣式也會一起幫你做出來。也就是說 WinJS 提供很多現成的效果可以直接使用，你不需要為了做出符合 windows 8 app 的 User Experience (比方說一些動畫的效果, 事件跟行為) 的效果而自己重造輪子。

---

###關於第三方的 Library 

* 這個部分是從 33 頁底下開始。
* Windows App 其實是可以讓你帶入一些第三方的 Library， 像是 jQuery, Modernizer, prototype.js 等等，但是有些功能是會被擋的，要記住的是，只用這些 library，必須把這些第三方的 library 也放在 package 裡面。（個人註解：我記得是不能像 web 一樣寫 CDN，比方說你要用jquery，那麼整個 jQuery 都要下載下來放到你的 package，可能是js資料夾或是哪裡之類的）。
* 雖然是用 web 的語言(html/css/JavaScript)寫的 app，可是跑在 WinRT 跟跑在 browser 是兩件事。
* 有些 JavaScript 的行為跟事件在 Win8 App 是會被擋住的，像是 `window.alert`, `windows.open`, `windows.prompt`等等，類似的功能你可以使用其他方式去取代，像 Windows.UI.Popups.MessageDialog 也是類似 windows.prompt 的功能。
* 你不能 load 外面的 script，也就是不能用 script src="https://source…" 來載入其他檔案，很有可能會被濾掉。
* windows 8 App 雖然也可以用 javascript 控制很多行為，不過有些 API 並不支援，請參考 [HTML 與 DOM API 變更清單](http://msdn.microsoft.com/library/windows/apps/hh700404.aspx)。
* 只有用 JavaScript 開發的 Windows 8 App 可以直接 access WinRT 這個 API，如果是用 C#, Visual Basic, C++ 還要 access Win32 跟 .NET API (這個 Win32 跟 .NET API 是什麼我就不懂了，有請大大們指示XDD)。

---

### Single-Page 對上 Multipage Navigation

* web 的做法，通常是有好幾個頁面，透過 `<a href="">go where</a>` 超連結轉到別的頁面，或是使用 location.href 做頁面的轉換，那…你覺得 app 怎麼轉頁呢？
* 在 App 你要用這種方式轉頁也是沒有問題，只是有些缺點，第一件事情是轉頁意味著要再 loading Script，還要重新 Parse HTML 檔案， render 畫面，如果要共用一些 global 變數是有點麻煩，而且還會有效能的問題。而且在 app 上轉頁其實是有點突兀的事情，因為這樣很難做到提供給 user 順暢的轉場效果。
* 所以，因為以上的種種因素，為了解決這些困擾，通常 app 都會是以 single HTML page 的方式，可能是有一塊主要的 Div，去替換 content，有點像是 ajax。

---

* 所以，傳統的桌面應用程式，跟 App 差在哪裡？ 答案是，後者的本質是有狀態的 (inherently stateful.---> 是這樣翻嗎？)。
* 後面有一段都在講 App State 跟 Roaming，不是很瞭解是在幹嘛的，暫時不寫。

---

### 祝大家 Happy Coding!
### 中秋佳節愉快！ 


今日進度結束，請等待下一篇。



如有任何問題，歡迎留言。雖然我不一定會 :P，但盡可能找到 reference 或解答。
