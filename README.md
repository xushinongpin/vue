# 作为一个全站工程师，前端需要继续学习嘚。

### vue网站：https://vuejs.org/

##### 挂载点内部的内容 - 模版内容 template

```
<body>
  <div id="template"></div>
</body>
  <script src="./js/vue.js"></script>
  <script type="text/javascript">
    new Vue({
      el:"#template",
      template:'<h1>hello {{msg}}</h1>',
      data:{
        msg:"world"
      }
    })
  </script>
```



