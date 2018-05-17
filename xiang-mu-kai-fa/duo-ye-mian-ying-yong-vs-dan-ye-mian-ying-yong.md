多页面应用   ：  页面跳转 - 返回html

有点：首屏时间块，SEO效果好

缺点： 页面切换慢



单页面应用    ：   页面跳转 ： JS渲染

优点： 页面切换块

缺点： 首屏时间稍慢，SEO差



```
点击切换
    <template>
        <div id="home">
            <div class="home">home</div>
            <router-link to="/list">列表页</router-link>
        </div>
    </template>
    
    <script>
        export default {
            name: "Home.vue"
        };
    </script>
    
    <style>
        .home {
            font-size: 50px;
        }
    </style>
```



