# 其他功能

## 定制侧边栏

在 `index.html` 中可以对Docsify 进行各种配置，详情参考[配置项](https://docsify.js.org/#/zh-cn/configuration)。我们可以定制一个自己的侧边栏 `_sidebar.md` 。默认情况下侧边栏会通过 Markdown 文件自动生成

``` html
<!-- index.html -->

<script>
    window.$docsify = {
        loadSidebar: true
    }
</script>
<script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
```

接下来就可以编辑 `_sidebar.md` 来显示自己的侧边栏。

`_sidebar.md` 的加载逻辑是从每层目录下获取文件，如果当前目录不存在该文件则回退到上一级目录。

## 显示目录

自定义侧边栏同时也可以开启目录功能。设置 `subMaxLevel` 配置项

``` html
<!-- index.html -->

<script>
    window.$docsify = {
         loadSidebar: true,
        subMaxLevel: 2s
    }
</script>
<script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
```

## 忽略副标题

当设置了 subMaxLevel 时，默认情况下每个标题都会自动添加到目录中。如果你想忽略特定的标题，可以在Markdown文件中给它添加 `<!-- {docsify-ignore} -->` 。
