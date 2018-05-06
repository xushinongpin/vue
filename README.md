# npm使用 安装nodejs 地址： https://nodejs.org/zh-cn/download/

1. build - 项目配置文件
2. config - 开发环境与线上文件的配置文件
3. node\_modules - 项目的依赖
4. src - 源代码放置的目录
   | main.js | 真个项目的入口文件 |
   | :--- | :--- |
   | App.vue |  |
5. static - 静态的资源
6. .babelrc
7. .editorconfig
8. .eslintignore
9. .eslintrc.js
10. .gitignore
11. .postcssrc.js
12. package.json
13. package-lock.json
14. index.html - 整个网站的最外层html
15. README.md

### vue网站：[https://vuejs.org/](https://vuejs.org/)

##### 挂载点内部的内容 - 模版内容 template

```
<body>
  <div id="template"></div>
</body>
  <script src="./js/vue.js"></script>
  <script type="text/javascript">
    new Vue({
      el:"#template",
      template:'<h1>hello {{msg}}</h1>',
      data:{
        msg:"world"
      }
    })
  </script>
```



