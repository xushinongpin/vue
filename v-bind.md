# v-bind 的简写是  ：

```
<body>
  <div id="v_bind"><div v-bind:title="title">hello world</div></div>
</body>
  <script src="./js/vue.js"></script>
  <script type="text/javascript">
    new Vue({
      el:"#v_bind",
      data:{
        title:"this is hello world",
      }
    })
  </script>
```



