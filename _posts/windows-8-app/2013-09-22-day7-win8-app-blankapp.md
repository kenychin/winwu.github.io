---
layout: post
category : Windows-8-app
title : Day7 介紹空白應用程式 Blank App
date: 2013-09-22 12:00:00
tagline: "HTML5 X JavaScript 開發 Windows 8 Apps"
tags : [windows 8 App]
---
{% include JB/setup %}

透過建立『空白應用程式』（Microsoft Design Blank App），我們來建立一些常見的 Windows UI 組件吧（總算可以開始寫一些code了XDD）！ 

這部分就先當做熱身，雖然這邊的介紹會比較碎片化，不過之後會介紹的 `Split App` 或是 `Grid App` 會有太多觀念要瞭解，一時之間我只好從最乾淨的 Blank App 講起。

雖然我說要來建立一些常見的 Window UI，但，怎麼知道到底有哪些 Windows UI 呢？完整到底有多少我也不清楚，不過有興趣的話可以看一下這個網址：[WinJS.UI Namespace](http://msdn.microsoft.com/en-us/library/windows/apps/br229782.aspx)。

之後可能會介紹這幾種：像 `AppBar`, `FlipView`, `Flyout`...等等。

---

以下，會先開始新專案，介紹一下資料夾的結構跟內容分別是做什麼的。

---

## 開始吧！
* 請開啓 Visual Studio，點選`『檔案』 →  『新增』 →  『專案』`（或直接按 Ctrl + Shift + N）。

<img src="https://raw.github.com/winwu/winwu.github.io/master/_site/images/Windows-8-app/day7-0.png"/>

__接著會出現起始畫面，選擇你要 App：__

	1. 請選擇你要建立『空白應用程式』（格線與分割會在後頭章節提到）。
	2. App名稱可自己命名，預設會是 App+數字（你開了第幾個App）。
	3. 位置預設會在 Visual Studio 2012/Projects 底下，你也可以自己調整。
	4. 勾消『為方案建立目錄』，（個人習慣），主要是我不習慣多產生一層資料夾。
	5. 按確定。

<img src="https://raw.github.com/winwu/winwu.github.io/master/_site/images/Windows-8-app/day7-1.png" width="100%"/>

* 這時候，會花幾秒鐘的時間幫你建立你的 App，完成之後就會看到這個畫面：

<img src="https://raw.github.com/winwu/winwu.github.io/master/_site/images/Windows-8-app/day7-2.png" width="100%"/>

__好了！ 等等呢，我們會在右側『方案總管』琢磨一下這個檔案下的內容。__

####現在先聊一些環境的設定：
1. 調整字型大小：
	
	在左下角有個100%可以將它調整高一點，讓文字變大。
	
<img src="https://raw.github.com/winwu/winwu.github.io/master/_site/images/Windows-8-app/day7-3.png" width="100%"/>

2. 顯示行號：

	選擇 『工具』 → 『選項』  → 『將顯示所有設定』 打開  →  選擇 文字編輯器 > 所有語言 > 一般。把『行號』打勾，若有需要自動換行的話，也可以一起設定。
	
<img src="https://raw.github.com/winwu/winwu.github.io/master/_site/images/Windows-8-app/day7-4.png" width="100%"/>
3. 編輯器的色系：
	如果也想要調成深色的話，打開`『工具』 → 『選項』→ 『環境』> 『一般』→ 『色彩佈景主題』`調整成深色。  
<img src="https://raw.github.com/winwu/winwu.github.io/master/_site/images/Windows-8-app/day7-5.png" width="100%"/>




### 空白應用程式(blank app)的檔案結構：
<img src="https://raw.github.com/winwu/winwu.github.io/master/_site/images/Windows-8-app/day7-6.png" width="50%"/>

* 空白應用程式 Blank App 是最基本的範本，基本也代表著這些檔案，可能是都是些很重
要的，挑幾個說：

---

* __package.appxmanifest__ 有點類似全站的設定檔，App名稱, App介紹, 列出這個 App 包含的文件，裡面還會需要設定一些logo的圖檔, 總共需要替換這幾個logo:

		* logo.png
		* smalllogo.png （小的logo）
		* storelogo.png (上架到市集的logo)
		* splashscreen.png (啓動應用程式時的畫面)

* __default.html__  是起始畫面，寫 web 的人會知道以前寫 default.html 也算是首頁的一種命名（default.html 會搭配 default.js，這些檔案會在 App 運行的時候使用到）
		
* __default.js__  這個檔案，用來處理整個 App 應用週期的程式碼（比方說啓動WinJS之類的），之後的範例也會很常在這裡寫Code。
	
* __css 資料夾__ 可以在這資料夾新增自己所需要的JavaScript File。
* __js 資料夾__ 可以在這資料夾新增自己所需要的JavaScript File。


* 官方文件有提到說，如果你是用 JavaScrip 開發 windows App，這些檔案都是基本且必備的。參考：[http://msdn.microsoft.com/zh-TW/library/windows/apps/hh986964.aspx](http://msdn.microsoft.com/zh-TW/library/windows/apps/hh986964.aspx)

####啓動/關閉 你的Blank App 

* 按鍵盤 F5 或工具列上的 
<img src="https://raw.github.com/winwu/winwu.github.io/master/_site/images/Windows-8-app/day7-7.png" width="20%"/>
執行於『本機電腦』

* 啓動之後你會先看到啓動畫面 (splashscreen.png) ，接著才會進入到內容的部分。
（啓動畫面）
<img src="https://raw.github.com/winwu/winwu.github.io/master/_site/images/Windows-8-app/day7-8.png" width="50%"/>

* 內容部分通常是黑底，然後什麼都沒有，因為我們也沒增加什麼內容。

* ok你已經做完了一件偉大的事情了，那就是看到你的Blank App真正跑起來的樣子。

* __接著怎麼關掉它呢？__
	* 若要關閉應用程式，從螢幕的上邊緣向下撥動直到下邊緣，或是按 `『Alt＋F4』`，另外如果你不小心進入到偵錯模式，那麼你會發現你可能無法編輯你的檔案，你必須先關掉偵錯，在 Visual Studio 中，按一下 `『偵錯』 > 『停止偵錯』` 用來關閉應用程式。

---

今日進度結束，下一篇來做些小東西。

如有任何問題，歡迎留言。雖然我不一定會 :P，但盡可能找到 reference 或解答。
