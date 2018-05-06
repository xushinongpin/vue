# 每个组件都是一个vue实例

##### 添加+删除 功能

```
  <body>
    <div id="root">
      <input v-model="inputValue" />
      <button @click="handleSubmit">提交</button>
      <ul>
        <todo-item v-for="(item , index) of list" :key="index" :content="item" :index="index" @delete="handleDelete"></todo-item>
      </ul>
    </div>
  </body>
  <script src="./js/vue.js"></script>
  <script type="text/javascript">
    Vue.component('todo-item',{
      props:['content','index'],
      template:'<li @click="handleClick">{{content}}</li>',
      methods:{
        handleClick:function(){
          this.$emit('delete',this.index)
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
        },
        handleDelete:function(index){
          this.list.splice(index,1);
        }
      }
    })
  </script>
```





