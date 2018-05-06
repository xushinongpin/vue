# v-if - 会消除dom节点，适合少次的显示隐藏  

# v-show - 性能相对更高一些，不用多次加载dom元素，适合进行多次隐藏或展示的内容 

# v-for - 用来控制一组数据，通过这组数据来循环显示dom结构

```
<body>
  <div id="root">
    <button @click="handleClick">toggle</button>
    <div v-if="show">hello world</div>
    <div v-show="show">hello world</div>
    <ul>
      <li v-for="(item, index) of list" :key="index">{{item}}</li>
    </ul>
  </div>
</body>
  <script src="./js/vue.js"></script>
  <script type="text/javascript">
    new Vue({
      el:"#root",
      data:{
        show:false,
        list:[1,2,3,1]
      },
      methods:{
        handleClick:function(){
          this.show = !this.show;
        }
      }
    })
  </script>
```



