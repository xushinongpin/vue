##### 添加下载iconfont 【 选择自己要的加入购物车，然后在购物车加进自己的项目，在项目中下载源码，将css给到的删掉自己从网上一共的样式代码复制下来  http://www.iconfont.cn/collections/index?spm=a313x.7781069.1998910419.4&type=1  】

```
header优化

<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back-icon">&#xe624;</div>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe632;</span>
            输入城市/景点/游玩主题
        </div>
        <div class="header-right">
            城市
            <span class="iconfont arrow-icon">&#xe6aa;</span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl";
  .header
    display: flex
    line-height: .86rem
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      padding-left: .2rem
      background: #fff
      border-radius: .1rem
      color: #ccc
    .header-right
      width: 1.24rem
      float: right
      text-align: center
      .arrow-icon
        margin-left: -.04rem
        font-size: .24rem
</style>


```



新建sytl文件 varibles.styl 定义变量

```
$bgColor = #00bcd4
```

修改webpack.base.conf.js文件自定义变量，就像@符一样

```

  resolve: {
    extensions: ['.js', '.vue', '.json'],
    alias: {
      'vue$': 'vue/dist/vue.esm.js',
      '@': resolve('src'),
      'styles': resolve('src/assets/styles'),
    }
  },
```

main.js修改

    // The Vue build version to load with the `import` command
    // (runtime-only or standalone) has been set in webpack.base.conf with an alias.
    import Vue from 'vue'
    import App from './App'
    import router from './router'
    import fastClick from 'fastclick'
    import 'styles/reset.css'
    import 'styles/border.css'
    import 'styles/iconfont.css'

    Vue.config.productionTip = false
    fastClick.attach(document.body)

    /* eslint-disable no-new */
    new Vue({
      el: '#app',
      router,
      components: { App },
      template: '<App/>'
    })




