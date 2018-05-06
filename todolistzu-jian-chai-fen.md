# 每个组件都是一个vue实例

```
  <body>
    <div id="root">
      <input v-model="inputValue" />
      <button @click="handleSubmit">提交</button>
      <ul>
        <todo-item v-for="(item , index) of list" :key="index" :content="item"></todo-item>
      </ul>
    </div>
  </body>
  <script src="./js/vue.js"></script>
  <script type="text/javascript">
    Vue.component('todo-item',{
      props:['content'],
      template:'<li @click="handleClick">{{content}}</li>',
      methods:{
        handleClick:function(){
          alert('111');
        }
      }
    })
    // var TodoTiem = {
    //   template:'<li>item</li>'
    // }
    new Vue({
      el:"#root",
      // components:{
      //   'todo-item':TodoTiem
      // },
      template:'',
      data:{
        inputValue:'',
        list:[]
      },
      methods:{
        handleSubmit:function(){
          this.list.push(this.inputValue);
          this.inputValue = '';
        }
      }
    })
  </script>
```



