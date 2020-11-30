# Docsify 使用体验

在开始之前不得不提的反而是[Gitbook](https://www.gitbook.com/)。作为一款结合来Git使用Markdown来进行文档编辑的项目，Gitbook使用广泛文档丰富还有可扩展性，本来深得我心，我使用Gitbook编写了部分笔记并进行了学习。但是运营团队现在已经全面将其商业化运营，对于Command Line Tool也停止了更新；同时，将Markdown文件编译成HTML格式后才能浏览以及编译后丑陋的文件布置实在是将我劝退。

这时，[Docsify](https://docsify.js.org/)偶然闯入了我的实现。纯粹的开源项目，在Github上已经斩获了上万star，最大的特点就是只对Mardown文件进行操作，不涉及编译。而且功能同样强大且轻量化。该有的功能一项不少，可扩展性也很强，十分能打。它的[中文官方文档](https://docsify.js.org/#/zh-cn/)就是利用Docsify生成的，十分详细，小白友好。

## 快速开始

### 全局安装

Docsify推荐全局安装 `docsify-cli` 工具，可以方便地创建及在本地预览生成的文档。

``` bash
    npm i docsify-cli -g
```

### 初始化项目

如果想在项目的 `./docs` 目录里写文档，直接通过 `init` 初始化项目。

``` bash
    docsify init ./docs
```

### 开始写文档

初始化成功后，可以看到 `./docs` 目录下创建的几个文件

- `index.html` 入口文件
- `README.md` 会做为主页内容渲染
- `.nojekyll` 用于阻止 GitHub Pages 忽略掉下划线开头的文件
直接编辑 `docs/README.md` 就能更新文档内容，当然也可以添加更多页面。

### 本地预览

在 `index.html` 目录下，通过运行 `docsify serve` 启动一个本地服务器，可以方便地实时预览效果。默认访问地址 `http://localhost:3000` 。
