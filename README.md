# 作为一个全站工程师，前端需要继续学习嘚。



1. build - 项目配置文件【 可以不动 】
2. config
3. node\_modules
4. src
5. static
6. .babelrc
7. .editorconfig
8. .eslintignore
9. .eslintrc.js
10. .gitignore
11. .postcssrc.js
12. package.json
13. package-lock.json
14. index.html
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



