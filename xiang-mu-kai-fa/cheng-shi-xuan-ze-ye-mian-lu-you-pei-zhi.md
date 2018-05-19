### router/index.js

```
import Vue from 'vue'
import Router from 'vue-router'
import Home from '@/pages/home/Home'
import City from '@/pages/city/City'

Vue.use(Router)

export default new Router({
  routes: [
    {
      path: '/',
      name: 'Home',
      component: Home
    }, {
      path: '/city',
      name: 'City',
      component: City
    }
  ]
})

```

### /pages/city/City.vue

```
<template>
  <city-header></city-header>
</template>

<script>
import CityHeader from './components/Header'
export default {
  name: 'City',
  components: {
    CityHeader
  }
}
</script>

<style lang="stylus" scoped>

</style>

```

### /pages/city/components/Header.vue

```
<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl";
  .header
    position: relative
    overflow: hidden
    height: $headerHeight
    line-height: $headerHeight
    text-align: center
    color: #fff
    background: $bgColor
    font-size: .32rem
    .header-back
      position: absolute
      top: 0
      left: 0
      width: .64rem
      text-align: center
      font-size: .4rem
      color: #fff
</style>

```

### /assets/styles/varibles.styl

```
$bgColor = #00bcd4
$darkTextColor = #333
$headerHeight = .86rem
```



