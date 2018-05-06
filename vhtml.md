# v-html  不转义，显示dom的内容

```
<body>
  <div id="v_html">
    <div v-html="content"></div>
  </div>
</body>
  <script src="./js/vue.js"></script>
  <script type="text/javascript">
    new Vue({
      el:"#v_html",
      data:{
        content:"<h1>hello</h1>",
      }
    })
  </script>
```



