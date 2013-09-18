---
layout: post
category : Windows-8-app
title : Day3  介紹 Windows 8 App 開發方式
tagline: "HTML5 X JavaScript 開發 Windows 8 Apps"
tags : [windows 8 App]
---
{% include JB/setup %}
## Day3  介紹 Windows 8 App 開發方式

* 這個章節主要是要介紹，Visual Studio 2012 可以讓你使用哪些語言去開發你要的 Windows Design 風格的應用（因為在此並不專指 Windows 8 App），Visual Studio 總共提供您以下幾種語言開發你要的應用程式：
	* JavaScript 搭配 HTML/CSS (適合web開發者)。
	* C#, Visual Basic, or C++ 搭配 XAML (適合開發 .NET Framework開發者)。
	* C++ 搭配 DirectX。

* (補充：DirectX 是一種圖形技術，也是windows8 的核心，它可以讓 windows8 保持畫面順暢的效果)

* 聰明的你，通常會選擇自己熟悉的語言下去開發，但我不是因為聰明，是因為以上我只會JavaScript，因此選用 JavaScript 去開發。

* 之後我們要注意的事情是，當你選用 JavaScript 去開發 App 的時候，整個 App 專案剛建立起來時，其整個檔案結構跟目錄，真的會是平常所熟悉的 html/css/js。


* 這時候前端的職業病就來了，哦？那是不是就沒有跨瀏覽器的問題了？ 沒錯。
那麼，可以載入 jQuery 嗎...，是可以，但會有些限制，這個之後的文章會提到。
* 例圖：一個空白應用程式的檔案目錄
* <img src="/_site/images/Windows-8-app/day3-2.png"/>

* 結構看起來雖然簡單，不過 JavaScript 的撰寫方式，以及你會在 html 裡看到很多以 `data-win*` 為首的自定義屬性，這個部分可有得研究的了！現在還不用急著瞭解，因為我也還沒看...之後，我們會透過不斷的建立『空白應用程式』（Microsoft Design Blank App），逐漸瞭解整個 App 是如何撰寫的。


* 之後，還會先介紹兩個在開發 windows 8 App 的 API，有點乏味...有點難懂...還請大家忍耐... 。

* 用 Visual Studio 開發其實有很多方便之處，像是 Windows 市集範本提供幾種配置方加入開發流程，透過一個叫做 WinJS 的 API，也可以讓我們動手寫出各種 windows 8 的元件或控制項。


* 參考：
[http://msdn.microsoft.com/en-us/library/windows/apps/bg125376.asp](http://msdn.microsoft.com/en-us/library/windows/apps/bg125376.asp)

---


今日進度結束。

如有任何問題，歡迎留言。雖然我不一定會 :P，但盡可能找到 reference 或解答。
