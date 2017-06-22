## for 循环优化技巧

- 常规实例：

```apple js
 for( var i=0;i<ary.length;i++){
     var container = document.getElementById('container');  
       container.innerHtml += 'my number: ' + i;  
       console.log(i);  
 }

* 缺点：
 每一次循环的时候都会重新的读取ary.length,并且循环内部
 每一次循环的时候也在从新定义变量获取元素，效率会严重的下降
 
```

- 优化实例：

```apple js
 var container = document.getElementById('container'); 
for(var i=0,len=ary.length;i<len;i++){
       container.innerHtml += 'my number: ' + i;  
       console.log(i);  
}

* 优点：
  初始定义了len变量等于ary.length，这样在之后的比较时就不用重新计算ary.length了，
  并且把循环体内部的变量提取到外部，达到了提高性能的目的

```