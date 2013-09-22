---
layout: post
title: "Node for Front End Developers - chapter01 讀書筆記"
date: 2013-09-22 21:00:00
tags : [node]
---
<img src="http://1.bp.blogspot.com/-aezAjcCEVVA/Uj7qyl_-6qI/AAAAAAAAEFQ/7xKG7b_nNi4/s640/IMG_0151.JPG" width="100%"/>

* 書籍資訊 : Node for Front-End Developers by Garann Means(O'Reilly).copyright 2012 Garann Means, 978-1-449-31883-3
* 參考網址：[Node for Front-End Developers](http://shop.oreilly.com/product/0636920023258.do)

##本書目錄：
1. Chapter 1 Getting Node Set Up
2. Chapter 2 Serving Simple Content
3. Chapter 3 Interaction with the Client
4. Chapter 4 Server-Side Templates
5. Chapter 5 Data Sources and Flow Control
6. Chapter 6 Model-View-Controller and Sharing Code


##我的前言
* 這本書今年暑假以600多元台幣購入（蠻貴的...），等了快兩週才寄來，至今才開始看:P
* 內容只有 6 個章節，僅僅45頁。
* 雖然 node 之於我，我並非熟手，但老實說這本書應該不像是給初學者看的，建議裝過 node.js，裝過 npm 的人看看。
* 作為 Front-End 寫 node.js，會有一些不適應症，我覺得這是正常的，但這也才是有趣的地方，一直要去想 How about write JavaScript on Back-End，跟自己所熟悉的 browser 的環境，完全是不同的兩世界。
* 輕鬆學就好，雖然目前工作沒有大量使用，不過 Nice to Know。

##這本書的特色，以及能給你的觀念...
1. 把 node 裝起來，如何 scaffolding 一個 web (所謂 scaffolding 就是鷹架，你可以把這裡的鷹架想像成一棟大樓的樑柱結構，如何快速建立一個具有基礎架構的 web Application)。
2. node 就像 web server。
3. 了解 node 怎麼接資料，在 php 我們用 `$_GET` 與 `$_POST` 接收 get 與 post 資料，那 node 呢？
4. 使用 `socket.IO` 實踐 realtime client-server 的溝通。
5. 使用 `template engine` 寫 web。（我還沒看到那個章節，不過就我所知的 template engine 有 EJS, Jade）。
6. 如何連接 database, 如何存資料。
7. 介紹 MVC（Model-View-Controller） pattern。


---

##Chapter 1
##Getting Node Set Up
###前言
* 說明 node 的安裝，本來 node 是裝在 Unix like 的作業系統，但現在 windows 也能裝了，看你的環境是什麼，就怎麼裝。
* 本書是假設讀者使用 Mac 的作業環境，但如果你不是，也不用擔心，如果有需要其他作業環境需要注意的事項，也會提及。


###Node 跟 NPM
* 安裝 Node 有很多種方式，可以從官網下載。[http://nodejs.org/](http://nodejs.org/)，你也可以用 git 下載：


	<pre>
	$ git clone git://github.com/joyent/node.git
	$ cd node
	$ git checkout v0.6.6
	$ ./configure
	$ make
	$ nake install</pre>
	>來源出處：Node for Front-End Developers by Garann Means(O'Reilly).copyright 2012 Garann Means, 978-1-449-31883-3 . page1
	
	* 利用 `git checkout vx.x.x` 是為了切換到穩定的 node 版本，你可以自由選擇你要切到什麼版本，利用 `git tag` 指令查看有哪些版本可用。

* 假如你想安裝 npm，可以直接透過 command-line : 
	
	`$ curl http://npmjs.org/install.sh | sh`。
* 什麼是NPM? npm 是 `N`ode `P`ackage `M`anager，這個 manager  包含了很多 node 的模組(Module)，以及第三方套件，讓你夠過一個指令就可以下載你要的套件。

###REPL
* Real-Eval-Print-Loop，這有點難解釋耶… 簡單來說就是可以在 command-line 直接打指令，就像我們會在 chrome 的 F12 (開發人員)的 console 打一些測試 JavaScript 的指令（ex:alert('AAA'); 或是 console.log('BBB');）的感覺，console 會直接回應你你所打的指令。
* 參考：[Read–eval–print loop-From Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop)
* 這裡之所以會提到 REPL 其實是因為 node 本身就是一個指令，如果你不知道你要執行哪一個檔案（application），你可以直接在 command-line 輸入 node，就會進入到 REPL 的模式，然後做一些簡單的運算他也會真的回應你，真的就跟瀏覽器的console蠻像的。

	<img src="http://4.bp.blogspot.com/-5CvnVXe4jdY/Uj75cgRK7gI/AAAAAAAAEFs/crxBXfTBVT4/s320/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7+2013-09-22+%E4%B8%8B%E5%8D%8810.08.52.png" />
	
* 如果你要跳出 REPL 模式必須按 `Ctrl`+`C`跳出（有的人必須按兩次）。
 
	<img src="http://2.bp.blogspot.com/-ScGkxoohjrI/Uj75cjV-ASI/AAAAAAAAEFo/UZf6HEAmXZY/s320/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7+2013-09-22+%E4%B8%8B%E5%8D%8810.09.06.png"/>
	>Ctrl+C 是什麼？ 這個關係到 Linux 的程序訊號（signal），所謂程序訊號就是送出一個訊號給某個程序，控制該程序的行為，因為 signal 有很多種，ctrl+c 其實就是一種訊號，該訊號是 SIGINT(2號)，代表著中斷或停止程序。


###File Organization
* 只要安裝了 node, 你就可以開始規劃你的 web application，你可以把資料放在任何地方。不過資料夾內的檔案結構，會希望你照著一些常見的規則去規劃，比方說 web application 的目錄下要有 `pacjage.json`, 甚至你的主程式的檔案會放在資料夾目錄下。
* 一些常見的目錄我們希望在目錄的第一層就看到：
	* node_modules : 放一些在你的 local 從 npm 所安裝的 modules
	* lib : 屬於這個 application 共用或是自訂的 modules
	* public / www / similar : 主要一些靜態檔案（static files），或是client-side用的一些檔案。


* 目錄的規劃全看你的需求，如果你要打造的是具有 MVC patter 的 web application，建議你的資料夾底下要有 `models`, `views`, `contollers` 這些資料夾。
* 如果你要使用像是 `Express` 這樣的 Framework ，通常你的目錄底下還有一個 routes 的資料夾。
* package.json 這個檔案蠻重要的，這個檔案會記錄你的 application 需要（會）跟哪些 module(模組) 具有相依性。
* package.json 寫起來會像這樣：

	<pre>
	{
	"name" : "myNode",
	"author" : "WinWu",
	"description" : "This is my node",
	"version" : "0.0.1",
	"dependencies" : {
		"express" : "2.5.x"
	},
	"engine" : "0.6.x",
	"main" : "app,js"
	}
	</pre>
	
	* dependencies 是蠻重要的一個部分，假如有一天把這個 web application 移到別的地方或目錄下，只需要透過 `npm install` 指令，就可以一次把所有這個 web application 所需要相依的 module 都安裝好。 
	* 關於 package.json ，以前我有寫過一篇文章，有興趣歡迎賞臉觀看 :P [node.js 一個package的檔案結構](http://yiyingloveart.blogspot.tw/2013/04/nodejs-package.html)


---

待續，下篇不知道會是什麼時候。
