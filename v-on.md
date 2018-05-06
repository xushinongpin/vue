

# v-on: 的简写方式是 @



##### 元素绑定事件 - 点击事件

```


<body>
  <div id="onclick">
    <div v-on:click="handleClick">{{content}}</div>
  </div>
</body>
  <!-- <script src="https://cdn.jsdelivr.net/npm/vue@2.5.16/dist/vue.js"></script> -->
  <script src="./js/vue.js"></script>
  <script type="text/javascript">
    new Vue({
      el:"#onclick",
      data:{
        content:"hello",
      },
      methods:{
        handleClick:function(){
          this.content = "world"
        }
      }
    })
  </script>
```



