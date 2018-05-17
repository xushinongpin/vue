# 可以理解为 ： 根据网址的不同，返回不同的内容给用户

    App.vue

      <template>
        <div id="app">
          <img src="./assets/logo.png">
          <router-view/> <!-- 显示的是当前路由地址所对应的内容  -->
        </div>
      </template>

      <script>
      export default {
        name: 'App'
      }
      </script>

      <style>
      #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
      }
      </style>

    main.js
        // The Vue build version to load with the `import` command
        // (runtime-only or standalone) has been set in webpack.base.conf with an alias.
        import Vue from 'vue'
        import App from './App'
        import router from './router'

        Vue.config.productionTip = false

        /* eslint-disable no-new */
        new Vue({
          el: '#app',
          router, //路由路径
          components: { App },
          template: '<App/>'
        })

    router.js
        import Vue from 'vue'
        import Router from 'vue-router'
        import HelloWorld from '@/components/HelloWorld'  // @标识src目录下

        Vue.use(Router)

        export default new Router({
          routes: [
            {
              path: '/',
              name: 'HelloWorld',
              component: HelloWorld
            }
          ]
        })




