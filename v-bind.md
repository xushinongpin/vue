# v-bind 属性绑定的简写是  ： ，v-model 双向数据绑定

```
<body>
  <div id="v_bind">
    <div v-bind:title="title">hello world</div>
    <input v-model="content"/>
    <div>{{content}}</div>
  </div>
</body>
  <script src="./js/vue.js"></script>
  <script type="text/javascript">
    new Vue({
      el:"#v_bind",
      data:{
        title:"this is hello world",
        content:"this is content",
      }
    })
  </script>
```



