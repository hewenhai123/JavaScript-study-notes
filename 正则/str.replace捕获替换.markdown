### 使用正则捕获组进行搜索和替换

~~~
   搜索本身是有用的，但是，当更改（或者替换）你匹配收到文本时，
你也可以使搜索功能更强大。
   你可以使用字符串中的 .replace()在字符串中搜索和替换文本。
.replace()的输入首先是你要搜索的正则表达式模式。
第二个数是替换匹配的字符串或一个执行某事件的函数。
~~~

```javascript
var wrongText = "The sky is silver.";
var silverRegex = /silver/;
wrongText.replace(silverRegex, "blue");
// 返回 "The sky is blue."

```

```javascript
var twinkleStar = "TwinkleStar,twinkleStar,TwinkleStar";
var starRegex = /Twinkle/g;
var result = twinkleStar.replace(starRegex,function(a,b,c,d){
    // a 匹配到的当前项
    // b当前项的index
    // c 所有匹配项 ->数组
  return str
})
```