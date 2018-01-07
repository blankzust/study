# try-catch语句

* 基本语法

```js
try {
  //可能会出现错误的代码
}catch(e){
  //在错误发生时进行的处理方式
}finally{
  //无论何时都可以执行
}
```

* finally语句注意点

`finally`是`try-catch`语句中可选的部分，但是如果有`finally`的话，无论`try-catch`中的代码是否包含了`return`语句，最终都要走向`finally`;如果写了`finally`语句，那么`catch`就是可选的，

```js
function test(){
  //如果写了finally语句，那么catch就是可选的
  try{
  return 'try'
  }catch(e){
    return 'actch'
  }finally{
    return 'finally'
  }
}
console.log(test()) // 输出结果finally
```



* ​

