#### axios基本使用
test2-11
1. 必须先导入才能使用：
`<script src="https://unpkg.com/axios/dist/axios.min.js"></script>`

`document.querySelector()` 获取元素
```
   axios.get(地址?key=value&key2=value2)
    .then(function(response){
        ...
    }),function(err){
        ...
    }
```
```
  axios.get(地址,{key:value,key2:value2})
    .then(function(response){
        ...
    }),function(err){
        ...
    }
```
2. 使用get或post方法即可发送对应的请求；
3. then方法中的回调函数会在请求成功或失败时触发；
4. 通过回调函数的形参可以获取响应内容，或错误信息；

#### axios+vue
1. axios回调函数中的this已经改变，无法访问data中数据；
2. 可以把this保存起来：`var that=this`，回调函数中直接使用保存的this即可；
3. 数据来源变成了网络请求得到的
 