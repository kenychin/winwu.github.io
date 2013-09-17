---
layout: post
category : Windows-8-app
title : Day3 [番外篇]Windows 8 UX Fundamentals Training Workshop 2012 影片筆記
date: 2013-09-17 11:00:00
tagline: "HTML5 X JavaScript 開發 Windows 8 Apps"
tags : [windows 8 App]
---
{% include JB/setup %}
## Day3 [番外篇]Windows 8 UX Fundamentals Training Workshop 2012 影片筆記
* 影片網址來源 ：[Windows 8 UX Fundamentals Training Workshop 2012](http://channel9.msdn.com/Events/Windows-Camp/Windows-8-UX-Fundamentals-Training-Workshop-2012)
* Windows 8 UX Fundamentals Training Workshop 2012 是一列的影片
* 以下是看影片的一些筆記：


---

##Windows UI 有以下幾點特色
	* 簡潔利落的排版風格
	* 內容重於形式 (Windows UI 的設計精髓是 Content Before Chrome)
	* 快速且流暢轉場效果
	* 動態磚
	* 橫向移動與Ｃ模型配置
	* 頁面具有階層式的導航模式，清楚的資料層級

###Ｃ模型配置示意圖
* C模型配置的特色是右邊是沒有邊框的，具有暗示使用者右邊還有內容的作用。
 ![C模型配置]({{ site.url }}/images/windows-8-app/day2-11.png)


---

##Windows 8 App Layout
對於 Layout 的排版方式，也是很講究的，請參考：[Windows-Dev Center - Windows Store apps : Laying out an app page](http://msdn.microsoft.com/en-us/library/windows/apps/hh872191.aspx)

針對上面的連結，我有稍微做了一點整理：

###Grid System 網格系統：
* 網格系統是由 `unit` 跟 `sub-units` 所組成，每一個 unit 約等於 `20 X 20` px 的正方體，每一個 unit 裡面可以包含 `16`個 `5 X 5` px 的 sub-units。

###Page Header 頁面標頭：
* 標頭的 baseline 應該要距離最上方 5 個 units 的大小（或者是跟最上方距離100px）， 標頭距離左側應該要有 6 個 units 的大小 (或者是跟左方距離120px)，標頭的字體是 SegoeUI Stylistic Set 20, light weight 。

###Content Region 中間區域：
* margin-top 約 7 個 units 的大小（或者說 140px）; left-margin 約 6 個 units 的大小（或者說 120px); margin-bottom 可以自由擴展，沒有限制。

###關於字型：
* 在開發任何 App，盡量使用統一的字型。
* 可以使用 Windows Library 的樣式表。
* Windows 8 App 所採用的首選字型是 `Segoe UI` (常用在按鈕或選擇器)，但首選的__中文字型__是	`微軟正黑體`，那麼到底什麼時候開採用什麼字型，官網有些說明，可以參考[字型的指導方針 (Windows 市集應用程式)](http://msdn.microsoft.com/zh-tw/library/windows/apps/hh700394.aspx)。
* JavaScript 的 Windows Library提供以下幾種 Segoe UI，差別在於粗細：(以下資料來自[字型的指導方針 (Windows 市集應用程式)](http://msdn.microsoft.com/zh-tw/library/windows/apps/hh700394.aspx))
	<ul>
	<li>Segoe UI Light：粗細為 200 的 Segoe UI。</li>
	<li>Segoe UI Semilight：粗細為 300 的 Segoe UI。</li>
	<li>Segoe UI：一般粗細 400 的 Segoe UI。</li>
	<li>Segoe UI Semibold：粗細為 600 的 Segoe UI。</li>
	<li>Segoe UI Bold：粗細為 700 的 Segoe UI。</li>
	</ul> 
* 當只要指定特定粗細的文字樣式時，可以這樣寫
	
	`<p style="font-family: 'Segoe UI Semibold'">Semibold text</p>`
* 關於字型的部分歡迎參考 [wiki Segoe](http://en.wikipedia.org/wiki/Segoe)

---

##一些 Windows 8 App 的畫面
為了怕沒有 window 8 的人不知道 window8 的一些畫面，所以截了一些圖片。

起始畫面，通常會看到畫面有很多`動態磚(Live Tile)`，win8 的四邊通常會藏有些功能，比方說右邊是`『系統快速鍵』`; 上下方是`『Application Bar (App Bar)』`(上方通常是導覽用途，下方通常是功能用途)，左邊是`『呼叫系統快速鍵』`（你開過沒有關的app會在左邊）。

 ![day2-1]({{ site.url }}/images/windows-8-app/day2-1.png)

 ![day2-2]({{ site.url }}/images/windows-8-app/day2-2.png)


###AppBar (Application Bar)
 ![day2-10]({{ site.url }}/images/windows-8-app/day2-10.png)

 ![day2-3]({{ site.url }}/images/windows-8-app/day2-3.png)
 
###表單元素
![day2-4]({{ site.url }}/images/windows-8-app/day2-4.png)

###Search Bar 搜尋框
![day2-5]({{ site.url }}/images/windows-8-app/day2-5.png)

###有 AppBar 的例子
![day2-6]({{ site.url }}/images/windows-8-app/day2-6.png)
![day2-7]({{ site.url }}/images/windows-8-app/day2-7.png)


---

###Windows 8 Strore 看看有哪些現成的作品
* (此圖截自：http://windows.microsoft.com/zh-tw/windows-8/apps#Cat=t1)
* 可以點選一些 App 看看裡面的內容。
![day2-8]({{ site.url }}/images/windows-8-app/day2-8.png)

---


* (此圖截自：http://apps.microsoft.com/windows/zh-tw/app/windows-8/d59f025f-8cf2-422e-b204-0684e9125501)
* 看看別人的 App 寫出來的樣子，這些都是很好的參考，我可能會最後會寫個 Windows 8 App 企劃書吧。
* ![day2-9]({{ site.url }}/images/windows-8-app/day2-9.png)

---

本來想寫一些 windows8 的操作/觸控方式，不過我沒有平板:P，此部分忍痛跳過。

###參考資源
* [http://msdn.microsoft.com/](http://msdn.microsoft.com/)
 

下一篇我還沒有想到要寫什麼，明天再看:P


本篇同時轉載於 [iT邦幫忙鐵人賽](http://ithelp.ithome.com.tw/ironman6/player/yiying/dev/1)。

如有任何問題，歡迎留言。雖然我不一定會 :P，不過會盡量解答。