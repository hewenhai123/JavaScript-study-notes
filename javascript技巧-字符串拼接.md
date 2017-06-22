## 字符串拼接技巧

> 构建字符串最优的方法，不要总想着for循环,最快的是join方法，在大数据量的情况下join最快，正则其次，最慢的是for循环

- 实例1：for循环
```apple js

var arr=['item1','item2','item3','item4'];
var arr2=[];
  for(var i=0;i<30;i++){
        arr2= arr2.concat(arr)
     }
var str="<ul>";
for(var i=0;i<arr.length;i++){
    str+="<li>"+arr[i]+"</li>";
   }
    str+="</ul>";
// console.log(str)
* 实例执行结果：
   time: 0.14794921875ms
   time: 0.15478515625ms
   time: 0.150390625ms
   time: 0.14501953125ms
   time: 0.10888671875ms
   平均值：0.14140625ms
```

- 实例2：join方法

```apple js
var arr=['item1','item2','item3','item4'];
var arr2=[];
  for(var i=0;i<30;i++){
        arr2= arr2.concat(arr)
     }
var str="<ul><li>"+arr.join("</li><li>")+"</li></ul>"
// console.log(str)
 time: 0.102783203125ms
 time: 0.1650390625ms
 time: 0.153076171875ms
 time: 0.162109375ms
 time: 0.0888671875ms
 平均值：0.134375ms
    

```



- 实例3：正则替换方法

```apple js
var arr=['item1','item2','item3','item4'];
 var arr2=[];
   for(var i=0;i<30;i++){
         arr2= arr2.concat(arr)
      }
   arr2="<ul><li>"+arr2+"</li></ul>";
   arr2=arr2.replace(/\,/g,"</li><li>");
 // console.log(str)   
  time: 0.1640625ms
  time: 0.13623046875ms
  time: 0.094970703125ms
  time: 0.161865234375ms
  time: 0.153076171875ms
  平均值：0.142041015615ms
  
```