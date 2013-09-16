---
layout: post
category : Windows-8-app
title : Day2:HTML5 X JavaScript 開發 Windows 8 Apps
date: 2013-09-17 19:00:00
tagline: "Day2 windows 8 的界面設計(Windows UI)"
tags : [windows 8 App]
---
{% include JB/setup %}
## Day2 windows 8 的界面設計(Windows UI)


大家看到 win8 的開始畫面，有沒有覺得一格一格的，裡面還有東西會亂動XD
有人稱他 `Metro Style` ，但我喜歡稱他 `Windows UI`，因為在開發 App 的時候，我都是用 `WinJS.UI` 去產生這些畫面上的元素，但也不是一定，你也可以很自由的設計你的界面。


---

##Windows UI 有以下幾點特色
	* 簡潔利落的排版風格
	* 內容重於形式
	* 快速且流暢轉場效果
	* 動態磚
	* 橫向移動

---

##Windows 8 App Layout
對於 Layout 的排版方式，也是很講究的，請參考：[Laying out an app page](http://msdn.microsoft.com/en-us/library/windows/apps/hh872191.aspx)

針對上面的連結，我有稍微做了一點整理：

###Grid System 網格系統：
* 網格系統是由 `unit` 跟 `sub-units` 所組成，每一個 unit 約等於 `20 X 20` px 的正方體，每一個 unit 裡面可以包含 `16`個 `5 X 5` px 的 sub-units。

###Page Header 頁面標頭：
* 標頭的 baseline 應該要距離最上方 5 個 units 的大小（或者是跟最上方距離100px）， 標頭距離左側應該要有 6 個 units 的大小 (或者是跟左方距離120px)，標頭的字體是 SegoeUI Stylistic Set 20, light weight 。

###Content Region 中間區域：
* margin-top 約 7 個 units 的大小（或者說 140px）; left-margin 約 6 個 units 的大小（或者說 120px); margin-bottom 可以自由擴展，沒有限制。

---

##一些 Windows 8 App 的畫面
為了怕沒有 window 8 的人不知道 window8 的一些畫面，所以截了一些圖片。

起始畫面，通常會看到畫面有很多`動態磚(Live Tile)`，win8 的四邊通常會藏有些功能，比方說右邊是`『系統快速鍵』`; 上下方是`『Application Bar (App Bar)』`(上方通常是導覽用途，下方通常是功能用途)，左邊是`『呼叫系統快速鍵』`（你開過沒有關的app會在左邊）。


<img src="../../images/windows-8-app/day2-1.png" width="100%"/>
<img src="../../images/windows-8-app/day2-2.png" width="100%"/>

###AppBar (Application Bar)
<img src="../../images/windows-8-app/day2-10.png" width="100%"/>

<img src="../../images/windows-8-app/day2-3.png" width="100%"/>

###表單元素
<img src="../../images/windows-8-app/day2-4.png" width="100%"/>

###Search Bar 搜尋框
<img src="../../images/windows-8-app/day2-5.png" width="50%"/>

###有 AppBar 的例子
<img src="../../images/windows-8-app/day2-6.png" width="100%"/>
<img src="../../images/windows-8-app/day2-7.png" width="100%"/>

---

###Windows 8 Strore 看看有哪些現成的作品
(此圖截自：http://windows.microsoft.com/zh-tw/windows-8/apps#Cat=t1)

可以點選一些 App 看看裡面的內容。
<img src="../../images/windows-8-app/day2-8.png" width="100%"/>

---


(此圖截自：http://apps.microsoft.com/windows/zh-tw/app/windows-8/d59f025f-8cf2-422e-b204-0684e9125501)
看看別人的 App 寫出來的樣子，這些都是很好的參考。
	<img src="../../images/windows-8-app/day2-9.png" width="100%"/>

---

本來想寫一些 windows8 的操作/觸控方式，不過我沒有平板:P，此部分忍痛跳過。

下一篇我還沒有想到要寫什麼，明天再看:P


本篇同時轉載於 [it邦幫忙](http://ithelp.ithome.com.tw/)。

如有任何問題，歡迎留言。雖然我不一定會 :P