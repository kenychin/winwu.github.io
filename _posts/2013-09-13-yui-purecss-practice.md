---
layout: post
title: "Pure CSS 實作練習(一)：Homepage"
date: 2013-09-13 21:00:00
tags : [HTML]
---

## Pure CSS 實作練習(一)：Homepage
這篇是延續好久好久以前寫的兩篇筆記，只是看看文章而已會讓我覺得學習中斷，感覺不是很好，後來我還是覺得想弄點什麼東西出來。之前的兩篇是這個：
- [認識 Pure CSS 之筆記一：了解Base, Grids, Forms ](http://yiyingloveart.blogspot.tw/2013/08/pure-css-base-grids-forms.html)
- [認識 Pure CSS 之筆記二：了解Buttons, Tables, Menus](http://yiyingloveart.blogspot.tw/2013/08/pure-css-buttons-tables-menus.html)

---
	
###練習的結果
主要是要練習 pureCSS 的 Grid，然後整格排版設計是參考某家搜尋網站的首頁做改造：P，icon 部分搭配的是 Font-Awesome ，Font-Awesome 的使用方式跟在用 bootstrap 的時候一樣，所以非常順手。至於配色就別跟我這個前端挑了（><），這個練習的重點是在做前端不是Art (Orz)。


*   [Demo Url](http://winwu.github.io/pureCSS-practice/homepage/)
*   [Github Repo 歡迎下載](https://github.com/winwu/pureCSS-practice)，不過手機上看還會跑版，還沒處理。
* 使用 Pure CSS 排列的一些樣板
* 關於 Pure 的使用方式，可至官網多瞭解 [http://purecss.io/](http://purecss.io/)
* 範本內有搭配 Font-Awesome [http://fortawesome.github.io/Font-Awesome](http://fortawesome.github.io/Font-Awesome)


###homepage Style
* Demo畫面1：（homepage/index.html）:
<a href="http://winwu.github.io/pureCSS-practice/homepage/"><img src="https://raw.github.com/winwu/pureCSS-practice/master/homepage/demo.png" alt="altTitle" title="" width="100%"/></a>

* Demo畫面2：
<img src="https://raw.github.com/winwu/pureCSS-practice/master/homepage/demo2.png" alt="altTitle" title="" width="100%"/>

###測試
* `Firefix`, `Chrome` is OK。
* 還不算是很成熟的作品，應該會找時間整理頁面。
* 如果你有任何建議歡迎留言補充。

###一些建議
pureCSS在他的網頁上有寫到，如果你要在 `grid-u-?-?` 的div裡加上 padding（除非你那塊沒有文字，不然很難不加 padding），它上面有寫到你可以這樣做（如果不這麼做寬度就會太多只至於div往下掉）：

```
.pure-g > div {  
     box-sizing: border-box;   
   } 
```
可是... 在我的 FireFox 整個大跑版，這時候你可以試試看補上-moz-box-sizing，如下範例。
[參考網址](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing)。


```
 .pure-g>div{  
   box-sizing: border-box;  
   -moz-box-sizing: border-box;   
 }  
```


###Author
* Author : Win Wu
* Blog : <http://yiyingloveart.blogspot.tw/>
* Update Date : 2013-08-31
* License : MIT License