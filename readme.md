
## 浏览器控制台可以执行脚本

目前的使用场景

        1、抖音直播中控台自动点讲解


###  快速上手


##### 1、复制代码


     var teswta1 = setInterval(function() {var xjyHTMLstr = document.getElementById("garSubApp").innerHTML;if (!!(xjyHTMLstr.match(/<button id=\"(\S*)\" .*?\<span\>取消讲解\<\/span>/)[1])) {console.log("找到了取消讲解");var buttonID = xjyHTMLstr.match(/<button id=\"(\S*)\" .*?\<span\>取消讲解\<\/span>/)[1];document.getElementById(buttonID).click();}setTimeout(function() {xjyHTMLstr = document.getElementById("garSubApp").innerHTML;if (!!(xjyHTMLstr.match(/<button id=\"(\S*)\" .*?\<span\>讲解\<\/span>/)[1])) {console.log("找到了讲解");var buttonID = xjyHTMLstr.match(/<button id=\"(\S*)\" .*?\<span\>讲解\<\/span>/)[1];document.getElementById(buttonID).click();}}, 3000);}, 12000);
    ;

     

##### 2、打开中控台，在浏览器里按f12打开开发者工具栏，切换到控制台那一页, 粘贴执行