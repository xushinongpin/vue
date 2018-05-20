### 运行打包命令 npm run build

### 根目录的dist目录就是要上线的代码，将它移动到后端根目录服务器

如果不想放在根目录，修改 /config/index.js build: {

    // Template for index.html

    index: path.resolve\(\_\_dirname, '../dist/index.html'\),



    // Paths

    assetsRoot: path.resolve\(\_\_dirname, '../dist'\),

    assetsSubDirectory: 'static',

    assetsPublicPath: '/',

.......

assetsPublicPath: '/', 改为 assetsPublicPath: '/你相放的目录',







