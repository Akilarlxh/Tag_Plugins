# Tag_Plugins——基于Butterfly主题的外挂标签魔改

1. 主要使用了[Volantis](https://github.com/volantis-x/hexo-theme-volantis)的标签样式。引入`[tag].js`，并针对`butterfly`主题修改了相应的`[tag].styl`。在此鸣谢`Volantis`主题众开发者。
2. 主要参考内容
  - [Volantis文档:内置标签插件](https://volantis.js.org/tag-plugins/)
  - [Butterfly 安装文档:标签外挂（Tag Plugins）](https://butterfly.js.org/posts/4aa8abbe/#%E6%A8%99%E7%B1%A4%E5%A4%96%E6%8E%9B%EF%BC%88Tag-Plugins%EF%BC%89)
  - [小弋の生活馆全样式预览](https://lovelijunyi.gitee.io/posts/c898.html)
  - [l-lin-font-awesome-animation](https://github.com/l-lin/font-awesome-animation)
  - [小康的butterfly主题使用文档](https://www.antmoe.com/posts/3b43914f/)

# 使用方法

1. 将下载的`Tag_Plugins.zip`解压得到`butterfly`文件夹。
2. 将`butterfly`文件夹复制到`[Blogroot]\themes\`目录下，覆盖当前的`butterfly`主题文件夹，提示重复则选择替换。(如果担心覆盖自己的其他魔改内容，可以根据静态文件内容自主比对修改)
3. 修改`[Blogroot]\_config.butterfly.yml`的`inject`配置项，添加`CDN`依赖项。由于`issues`写入`timeline`和`site-card`标签要用到`jquery`，请务必根据注释指示的版本决定是否添加。
  ```yml
inject:
  head:
    - <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/l-lin/font-awesome-animation/dist/font-awesome-animation.min.css"  media="defer" onload="this.media='all'">  #动画标签anima的依赖
  bottom:
    - <script defer src="https://cdn.jsdelivr.net/npm/jquery@latest/dist/jquery.min.js"></script>
    # 自butterfly_v3.4.0+开始，主题基本实现去jquery化，需要自己添加引用，请读者根据版本自行决定是否添加这行引用。
    - <script defer src="https://cdn.jsdelivr.net/npm/hexo-theme-volantis@latest/source/js/issues.min.js"></script>
    #数据集合标签issues的依赖
  ```

# 语法手册

详细使用手册请参看[Akilarの糖果屋-基于Butterfly的外挂标签引入](https://akilar.top/posts/615e2dec/)
