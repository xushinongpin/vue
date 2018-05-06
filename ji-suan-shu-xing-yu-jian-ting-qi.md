# 计算属性-computed 与 监听器-watch

```
<body>
  <div id="root">
    <input v-model="first" />
    <input v-model="last" />
    <div>{{full}}</div>
    <div>{{count}}</div>
  </div>
</body>
  <script src="./js/vue.js"></script>
  <script type="text/javascript">
    new Vue({
      el:"#root",
      data:{
        first:"",
        last:"",
        count:0
      },
      computed:{
        full:function(){
          return this.first + ' ' +this.last
        }
      },
      watch:{
        full:function(){
          this.count++
        },
      }
    })
  </script>
```



