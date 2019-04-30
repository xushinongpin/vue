# GitHub地址： [https://github.com/xushinongpin/vue](https://github.com/xushinongpin/vue)

# npm使用 安装nodejs 地址： [https://nodejs.org/zh-cn/download/](https://nodejs.org/zh-cn/download/)

# 后台

1. ## [php部分笔记](https://php.lvtian.vip/)
2. ## [tp几个坑](https://tp.lvtian.vip/)
3. ## [**laravel初学笔记**](https://laravel.lvtian.vip)
4. ## [learnku初学笔记](https://learnku.lvtian.vip/)
5. ## [learnku开发实战进阶](https://learnku-2.ilvtian.vip/)
6. ## [learnku电商实战 ](https://learnku-shop.ilvtian.vip/)
7. ## [多租户笔记](https://multi-tenant.lvtian.vip/)
8. ## [微信-没用](https://wechat.lvtian.vip/)
9. ## [微擎备忘-没用](https://weiqing.lvtian.vip)

# 前台

1. ## [layui备忘笔记](https://layui.lvtian.vip/)
2. ## [vue笔记](https://vue.lvtian.vip/)

# 运维

1. ## [centos学习](https://linux_centos.lvtian.vip/)
2. ## [平常遇到的坑与生活笔记](https://net.lvtian.vip/)

# seo

1. ## [seo学习笔记](https://seo.lvtian.vip/)

# Python

1. ## [Python学习笔记](https://python.lvtian.vip/)

```
├── build                      // 构建相关  
├── config                     // 配置相关
├── src                        // 源代码
│   ├── api                    // 所有请求
│   ├── assets                 // 图片 字体等静态资源
│   ├── components             // 全局公用组件
│   ├── directive              // 全局指令
│   ├── filtres                // 全局filter
│   ├── mock                   // mock数据
│   ├── router                 // 路由
│   ├── store                  // 全局store管理
│   ├── styles                 // 全局样式
│   ├── utils                  // 全局公用方法
│   ├── views                  // view
│   ├── App.vue                // 入口页面
│   ├── main.js                // 入口 加载组件 初始化等
│   └── permission.js          // 权限控制 初始用户数据等
├── static                     // 第三方不打包资源
│   ├── img                    // 第三方不打包图片
│   └── theme                  // 主题包
├── .babelrc                   // babel-loader 配置
├── eslintrc.js                // eslint 配置项
├── .gitignore                 // git 忽略项
├── .fjpublish.config.js       // 自动化发布服务器 配置
├── index.html                 // html模板
└── package.json               // package.json
vue网站：
https://vuejs.org/

vue-router 文档地址：   
https://router.vuejs.org/zh-cn/
 【 安装： npm install vue-router 】
vue-resource 的GitHub地址：  
https://github.com/pagekit/vue-resource
 【 安装： npm install vue-resource 】
安装stylus和stylus-loader 【 npm install stylus stylus-loader --save-dev 】
icon.styl里面路径踩过的坑：
    ../fonts/sell-icon.eot... 不能写相对路径，要改为绝对路径 - 
    /src/common/fonts/sell-icon.eot...
css3 注意事项网址：  
https://www.w3cplus.com/css3/css-secrets/sticky-footers.html

flex布局 分享网址： 
http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html

挂载点内部的内容 - 模版内容 template
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



