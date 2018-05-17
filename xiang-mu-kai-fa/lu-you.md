# 可以理解为 ： 根据网址的不同，返回不同的内容给用户

```
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

```



