HTML5 程式設計 學習日誌
===

## 簡介
<font color="#FA8072">**中興大學110學年度上學期HTML5的學習日誌、作業解題思路
快速跳轉請按左側的目錄欄!**</font>
:::info
:mega: 作業解題思路 要去看 :mega:
:::

## 上課日誌
### 第二週(09/27)
第一週為中秋連假，放假一次，故從第二週開始上課。
上課內容:
> 認識基本的html結構，如head、body，
> 以及html的語法，如heading、paragraph。

一個最基本的html架構如下，要用```<html>```，裡面包著```<head>```和```<body>```。
```<h1>...</h1>```中間夾著的是放標題文字(依照標題字體大到小，可使用```h1~h6```)。
```<p>...</p>```中間夾的是內文，會印出中間夾的文字。

合併以上內容就會變成下面這個架構:

```htmlmixed=
<html>
    <head>
      ...
    </head>
    
    <body>
        ...
        <h1>Headings</h1> <!--標頭文字-->
        <p>paragraph</p> <!--內文-->
        ...
    </body>
</html>
```

### 第三週(10/04)
上課內容:
> 介紹image、Hyperlinks、button等語法，再加上javascript的function、array
> 之後就可以implement相片切換瀏覽功能

<font color="red"> **Note:** 更多張圖片輪播的例子我寫在下面 **[作業一](https://hackmd.io/9q5AE1IERl65waaJDM-dFw?both#%E7%AC%AC%E4%B8%80%E6%AC%A1%E4%BD%9C%E6%A5%AD1004)** 和 **[作業二](https://hackmd.io/9q5AE1IERl65waaJDM-dFw?both#%E7%AC%AC%E4%BA%8C%E6%AC%A1%E4%BD%9C%E6%A5%AD1018)** </font>
<font color="red"> **Note:** 更多張圖片輪播的例子我寫在下面 **[作業一](https://hackmd.io/9q5AE1IERl65waaJDM-dFw?both#%E7%AC%AC%E4%B8%80%E6%AC%A1%E4%BD%9C%E6%A5%AD1004)** 和 **[作業二](https://hackmd.io/9q5AE1IERl65waaJDM-dFw?both#%E7%AC%AC%E4%BA%8C%E6%AC%A1%E4%BD%9C%E6%A5%AD1018)** </font>
<font color="red"> **Note:** 更多張圖片輪播的例子我寫在下面 **[作業一](https://hackmd.io/9q5AE1IERl65waaJDM-dFw?both#%E7%AC%AC%E4%B8%80%E6%AC%A1%E4%BD%9C%E6%A5%AD1004)** 和 **[作業二](https://hackmd.io/9q5AE1IERl65waaJDM-dFw?both#%E7%AC%AC%E4%BA%8C%E6%AC%A1%E4%BD%9C%E6%A5%AD1018)** </font>

用上面的這些工具，就可以做到照片輪播，下面是最基本兩張照片輪播的例子([jsbin](https://jsbin.com/vibehugoqa/1/edit?html,output)):
```htmlmixed=
<html>
    <head>
        <!--javascript的部分-->
        <script>
            function f1() {
                document.getElementById("x").innerHTML = '<img src="https://pbs.twimg.com/media/EWy2bgzU0AAYain.png"  width="100%">' 
            }
            function f2() {
                document.getElementById("x").innerHTML = '<img src="https://dailystatuss.com/wp-content/uploads/2021/05/75412686_2196575703971486_5469967625223337543_n-1024x1024.jpg" width="100%">' 
            }
	</script>
    </head>

    <body>
        <div id="x">
            <!--最一開始呈現的第一張-->
	    <img src="https://pbs.twimg.com/media/EWy2bgzU0AAYain.png" width="100%">
        </div>
        <!--用Hyperlink跳到別張圖片-->
        <a href="javascript:f1();">上一張</a>
        <a href="javascript:f2();">下一張</a>
    </body>
</html>
```

### 第五週(10/18)
第四週為連假，放假一天。
上課內容:
>檢討作業(一些在語法、排版上可以改進的小地方)
>Date() 的用法
>JavaScript Timing Events: setTimeout()、setInterval()
```
作業檢討的例子:
1. 縮排和註解: if判斷式中的空格要記得加，才比較好讀
    if ( aa==0 && bb>0 ) {
        //註解加在這裡
    }
    
2. 避免重複的敘述
    if (條件) {
        敘述A; //不好的示範
    }
    else {
        敘述A; //不好的示範
    }
    
    //建議改成下面的，把敘述A拿出來
    if (條件) {...}
    else {...}
    敘述A;
    
3. variable能放local的話就不要放在global，容易重複命名導致出大事
```

### 第六週(10/25)
>Material CSS的
>Navbar、Footer：one page的head、foot
>Grid：縮放螢幕比例，一個row呈現的data數也會跟著增減
>Card：和Grid結合，即可做出類似購物網站呈現商品的介面 

**<font color="indigo">Note: 使用for loop去顯示多個商品，如 [HW3的片段](https://hackmd.io/9q5AE1IERl65waaJDM-dFw?both#%E7%AC%AC%E4%B8%89%E6%AC%A1%E4%BD%9C%E6%A5%AD1025) </font>**
**<font color="indigo">Note: 使用for loop去顯示多個商品，如 [HW3的片段](https://hackmd.io/9q5AE1IERl65waaJDM-dFw?both#%E7%AC%AC%E4%B8%89%E6%AC%A1%E4%BD%9C%E6%A5%AD1025) </font>**
**<font color="indigo">Note: 使用for loop去顯示多個商品，如 [HW3的片段](https://hackmd.io/9q5AE1IERl65waaJDM-dFw?both#%E7%AC%AC%E4%B8%89%E6%AC%A1%E4%BD%9C%E6%A5%AD1025) </font>**

這樣就可以避免每個商品都要一直重複寫類似的敘述，如下
```javascript=
for (i = 0; i < picture.length; i++) {   
          text += '<div class="col s12 m4 l2">';
          text += '  <div class="card">';
          text += '    <div class="card-image">';
          text += '      <img src="'+picture[i]+'">'
          text += '    </div>';
          text += '    <div class="card-content">';
          text += '      <p>第'+(i+1)+'套</p>';
          text += '    </div>';
          text += '    <div class="card-action">';
          text += '      <p>'+clothes[i]+'</p>';
          text += '    </div>'
          text += '  </div>';
          text += '</div>'; 
}
```

### 第七週(11/01)
> 資料庫的概念

利用 **[regular expression](https://www.w3schools.com/js/js_regexp.asp)** 的概念找到網址中的特定資訊(ex.產品ID)，用來傳入資料庫，找參數們的方式：
```
取得網址列的內容:
window.location.href

網址內的特殊符號與中文字在傳遞前後需要做的一些處理:
decodeURIComponent() 和 encodeURIComponent()
```
再用老師給的[這個例子](http://jsfiddle.net/2x80jm8a/)來解析網址參數。

補充: 可以將要放在一起的html檔上傳到[netlify](https://app.netlify.com/teams/bettyteng21/overview)上面。

**<font color="indigo">Note: 使用前面講的東西，套用到之前的作業三，如 [HW4](https://hackmd.io/9q5AE1IERl65waaJDM-dFw?both#%E7%AC%AC%E5%9B%9B%E6%AC%A1%E4%BD%9C%E6%A5%AD1101) </font>**
**<font color="indigo">Note: 使用前面講的東西，套用到之前的作業三，如 [HW4](https://hackmd.io/9q5AE1IERl65waaJDM-dFw?both#%E7%AC%AC%E5%9B%9B%E6%AC%A1%E4%BD%9C%E6%A5%AD1101) </font>**
**<font color="indigo">Note: 使用前面講的東西，套用到之前的作業三，如 [HW4](https://hackmd.io/9q5AE1IERl65waaJDM-dFw?both#%E7%AC%AC%E5%9B%9B%E6%AC%A1%E4%BD%9C%E6%A5%AD1101) </font>**

作業四的其中一小段:
```javascript=
for (i = 0; i < picture.length; i++) { 
    text += '<div class="col s12 m4 l3">';  
    text += '  <div class="card hoverable">';
    text += '    <div class="card-image">';
    text += '      <a href="description.html?id='+i+'"> <img src="'+picture[i]+'" width="100%">'
    text += '    </div>';
    text += '    <div class="card-content indigo lighten-5">';
    
    ///////////////////////////////////
    //這行就是利用id，跳到商品的詳細介紹
    //在執行此HTML的網址最後加上 "?XXX=你要傳遞的字串
    text += '	    <a class="indigo-text text-darken-3" href="description.html?id='+i+'">'+title[i]+'</a>';
    //////////////////////////////////
    
    text += '	  </div>';
    text += '  </div>';
    text += '</div>';
}
```


### 第八週(11/08)
>將google form當成小型的資料庫，新增資料在裡面。
>利用matirialize css的東西去建立可輸入東西的格子，以及radio button等
>還有順便提到如何去改icon

套用今天教的到作業上: 
在兩欄分別輸入劇名以及推薦理由，即可自動填入google form並送出

<img src="https://i.imgur.com/ICTpE0A.png" alt="drawing" width="200"/><br/> 

程式碼如下
```html=
<!--google表單填寫-->
<span id="formresponse"></span>
<div class="row">
    <div class="container" style="width: 85%;height: 100%;max-width: 100%;margin: auto;">
	<form class="col s12"name="form1" action="javascript:formresponse();">
	    <div class="row">
		<div class="input-field col s4">
		    <i class="material-icons prefix">favorite_border</i>
		    <input type="text" name="recommend">
		    <label for="icon_prefix">推薦劇名</label>
		</div>
	    </div>
	    <div class="row">
		<div class="input-field col s4">
		    <i class="material-icons prefix">feedback</i>
		    <input type="text" name="reason">
		    <label for="icon_telephone">推薦理由</label>
	        </div>
	    </div>
	    <input type="submit" value="Submit">
	</form>
    </div>
</div>
```

### 第十一週(11/29)
>如何讀取google試算表的資訊

<font color="indigo">**我把這次教的套在作業四的index.html裡: [連結](https://jsbin.com/yuzedojuje/edit?html,output)** </font>
<font color="indigo">**我把這次教的套在作業四的index.html裡: [連結](https://jsbin.com/yuzedojuje/edit?html,output)** </font>
<font color="indigo">**我把這次教的套在作業四的index.html裡: [連結](https://jsbin.com/yuzedojuje/edit?html,output)** </font>

先把之前作業中的array放到試算表:
<img src="https://i.imgur.com/Okbqxu4.png" alt="drawing" width="200"/>


當load完goolge visualization API之後，即可開始使用，例子如下:
```javascript=
function processSheetsData(response) {
    var data = response.getDataTable();
    var columns = data.getNumberOfColumns();
    var rows = data.getNumberOfRows();
          
    var text="";
    for (var i = 1; i < rows; i++) { //第0列是標題
      ...
        text += '    <div class="card-image">';
        text += '      <a href="description.html?id='+i+'"> <img src="'+data.getFormattedValue(i,0)+'" width="100%">'
        text += '    </div>';
        text += '    <div class="card-content indigo lighten-5">';
        text += '	<a class="indigo-text text-darken-3" href="description.html?id='+i+'">'+data.getFormattedValue(i,1)+'</a>';
        text += '    </div>';
      ...
    }
    document.getElementById("demo").innerHTML = text;
}

```

### 第十二週(12/06)
>教如何使用iframe崁入google map

```
設定超連結到 http://maps.google.com.tw/maps?f=q&hl=zh-TW&geocode=&q=經緯度座標或地址&z=比例&t=h衛星圖或p地形圖&output=embed

例子:
設我的經緯度座標是(24.121618032245966,120.67646410790938)
那麼iframe使用的網址:
https://maps.google.com.tw/maps?f=q&hl=zh-TW&geocode=&q=24.121618032245966,120.67646410790938&z=15&t=p&output=embed
```

z是代表google map的縮放比例，z越大地圖放越大

<font color="indigo"> **套用今天教的套到第四次作業(加上拍攝地點): [連結](https://4108056007.netlify.app/description.html?id=0)** </font>
<font color="indigo"> **套用今天教的套到第四次作業(加上拍攝地點): [連結](https://4108056007.netlify.app/description.html?id=0)** </font>
<font color="indigo"> **套用今天教的套到第四次作業(加上拍攝地點): [連結](https://4108056007.netlify.app/description.html?id=0)** </font>

### 第十三週(12/13)
>可以套用materialize css的免費版型

可參考網站: **[連結1](https://materializecss.com/getting-started.html#templates)**、**[連結2(直接下載code然後自己試著改)](https://github.com/Erickmateli/materialize-css-template)**

自己修改的例子:
將 **[連結2](https://github.com/Erickmateli/materialize-css-template)** 的三個並列的card套用在for loop，將圖片連結放到array中
(這樣就不用同一個card寫三遍)
<img src="https://i.imgur.com/y5laaTZ.png" alt="drawing" width="200"/>

```javascript=
//Note: 下面是pseudo code，實際的code還要把這些改成string
var a =["team1.png", "team2.png", "team3.png"];
for(i=0; i<3; i++){
 <div class="col s12 m4 l4  center-align">
    <div class="card-panel blue darken-1">
      <img src= a[i] alt=""> //////用array存放圖片//////
      <div class="team1border">
      </div>
      <li class="white-text" id="teamname">Faridul Haque</li>
      <li class="white-text" id="teamrole">Graphic Designer</li>

      <div class="team2border">
      </div>
      <i class="mdi mdi-facebook mdi-24px white-text"></i>
      <i class="mdi mdi-twitter mdi-24px white-text"></i>
      <i class="mdi mdi-linkedin mdi-24px white-text"></i>
      <i class="mdi mdi-google mdi-24px white-text"></i>
    </div>
  </div>
}
```

### 第十四週(12/20)
>痞客幫API基本功
>json格式及轉換

若網址為: https://emma.pixnet.cc/mainpage/blog/categories/hot/23?page=1&per_page=10&api_version=2&format=json

最後面有寫```format=json```，代表是json格式。
json格式一樣會把網頁資訊儲存起來(ex. 圖片、文字)，只是寫法不同而已，又因為json格式不太好閱讀，所以可以使用 **[json parser](http://json.parser.online.fr/)** 來轉換成更容易閱讀的排版。
```javascript=
function myFunction(arr) {
    var data = arr.articles; //網頁的東西都放在articles裡面
    var out = "";
    var i;
    for (i = 0; i < data.length; i++) {
	if ( data[i].thumb != "" ) //簡單防呆 
            out += '<img src="' + data[i].thumb + '" />';
            //縮圖是放在articles裡的thumb
	if ( data[i].title != "" ) //簡單防呆
            out += '<p><a href="' + data[i].link + '" target="_blank">' + data[i].title + '</a></p>';
            //文章連結是放在articles裡的link
	out += '<p> </p>';
	if ( data[i].tags.length != 0 ){ //簡單防呆
	    out += '<p>Tags: ';
		for (j = 0; j < data[i].tags.length; j++) {
                //tag可能有很多個，所以用for迴圈去跑
		    out += data[i].tags[j].tag + ', ';
                    //文章hash tag連結是放在articles裡的tag
		}
		out += '</p>';
	}
	out += '<br /><br /><br />';
    }
    ...
}
```

---------------------------------------------
## 作業解題思路
### 第一次作業(10/04)
作業第一階段: **[連結](https://jsbin.com/bonicot/edit?html,output)**
```
採用array去存圖片的link，當到頭尾時即無法再往下。
```
作業第二階段: **[連結](https://jsbin.com/murixug/edit?html,output)**
```
採array去存圖片的link，circular的方式放映。
用modulo去計算index: i = ((i % x.length)+x.length) % x.length;
(x為圖片的array)
```
計算index的例子:
```
i+=y;
i = ((i % x.length)+x.length);

設i+=y完的i=-3，且有4張圖片
先做(i % x.length) => i=-3
再加x.length => i=1
再mod x.length => i=1
最終得到i=1

更簡單的寫法
i = ((i+1) + x.length) % x.length;
```

### 第二次作業(10/18)
作業: **[連結](https://jsbin.com/fajasedima/edit?html,output)**
```
Based on 作業1的part2，增加開始、結束自動輪播的功能。
使用setInterval()去實作
```
我多增加了一個boolean變數resume_auto_play，true代表目前正在放映。
設立原由: 

>如果我正在放映，然後手動點上一頁，setInterval()的計時器仍在繼續countdown，所以很快就會變換圖片，但是我想要讓計時器重新countdown

使用時機:
```javascript=
function manual_play(y){ //手動輪播
    ...
    if( resume_auto_play == true ){ 
    //手動輪播前 正在自動輪播 所以手動操作完恢復自動輪播
        photo_player=setInterval(auto_play, 3000);
    }
    ...
}
```

另外也新增一個隨機放映的button，使用Math去隨機產生0~3的index
```javascript=
function auto_shuffel_play() { //隨機輪播
    //我要取的index如下
    ... x[Math.floor(Math.random() * x.length)] ...; 
}
```

### 第三次作業(10/25)
作業: **[連結](https://jsbin.com/sogofelona/edit?html,output)**
```
做出一個像購物網站那樣，有產品、discription、link等等
還可以增加一些小功能、改一些顏色什麼的
```
這次是做某電視劇男主角的劇中造型，將出現過的衣服代替商品去呈現，
所以Navbar的標題是寫"周生辰的衣櫃"。
多增加的東西: 在footer加上靠右的電視劇logo image。
網頁中的link buttons都是相關的東西，可以點進去看看！

### 第四次作業(11/01)
作業: **[code在github HW4的資料夾](https://github.com/bettyteng21/1101-HTML5)**
網頁預覽: **[連結](https://4108056007.netlify.app/)**
本次作業用到的圖片: **[imgur連結](https://bettyteng21.imgur.com/all)**

```
改善上次作業
按連結即可跳轉一個新的頁面，新頁面中有商品圖片、商品介紹
可以再加上一些materialize css
```
本次作業多增加的廢廢小東西:
```
1. 改字體!!用了一個手寫感的字體(花好久研究怎麼import...解決方式如下連結)
2. 滑鼠游標到card會產生陰影(hover)
3. 新頁面有youtube的小小播放視窗
4. 按新頁面的logo就會回到首頁(上一頁)
5. 點進新頁面中的圖片，會有圖片完整大小的劇照
6. (12/06新增) 加上拍攝地點，利用google map的iframe
```

遇到的問題以及改善方式，請參考連結: 
[card高度不一致，導致無法對齊](https://stackoverflow.com/questions/46064332/materialize-cards-not-on-equal-height)
[如何import從網路上下載的字體檔](https://stackoverflow.com/questions/11737168/how-to-import-fonts-in-css)
[如何返回上一頁](https://stackoverflow.com/questions/8814472/how-to-make-an-html-back-link)

### 期末作業
**最終的網頁: https://4108056007.netlify.app**

各式的表單:
**[儲存商品資料的spreadsheet](https://docs.google.com/spreadsheets/d/11TP680c-btT7WzdvkKKz6moEfbpHK6aaztWH0j0pWdM/edit#gid=0)**
**[給用戶填寫的意見表](https://docs.google.com/forms/d/1RMBDqEy78zj2fodTEGh6HnuCywCG1IbBIIHI9hBIMug/edit)**
**[意見表匯出的spreadsheet](https://docs.google.com/spreadsheets/d/1nsgAFVXiQaUGBaSv_vgNPRugesst5uU8Qey4f0h2iy4/edit?resourcekey#gid=1605649634)**
```
期末的基本requirements
1. 首頁主題明確、版面美感、具有通往各子頁選項
2. 至少一個頁面以試算表為資料庫呈現內容摘要列表(如Gomaji商品列表)、點擊單項以網址傳遞參數方式呼叫內容介紹頁面(內容資料仍應取得試算表資料方式呈現)
3. 建立表單資料輸入後直入試算表，後續有個頁面可列出輸入資料。
4. 將地圖呈現融入某個頁面內容(仍應取得試算表資料方式呈現)
5. 將PIXNET API呈現資訊融入某個頁面
```


---

更多內容請到 **[我的github](https://github.com/bettyteng21)**

