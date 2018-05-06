# v-text  将内容转义，将标签也看成文本

```
<body>
  <div id="v_text">
    <div v-text="content"></div>
  </div>
</body>
  <script src="./js/vue.js"></script>
  <script type="text/javascript">
    new Vue({
      el:"#v_text",
      data:{
        content:"<h1>hello</h1>",
      }
    })
  </script>
```



