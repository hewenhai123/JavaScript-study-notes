### str.match(reg)

~~~
   reg.test()方法只是检查了字符串中是否存在模式。
   还可以使用match（） 方法找到实际的匹配项。
   .match()方法返回值是一个数组。
   
~~~

```javascript
var extractStr = "Extract the word 'coding' from this string.";
var reg=/coding/;
var result=extractStr.match(reg);
```

---

