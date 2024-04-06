# Hexo

> 使用 Hexo + GitHub Pages 搭建一个**静态网站**

官方网址：https://hexo.io/zh-cn/

官方文档：https://hexo.io/zh-cn/docs/

## 安装 Node.js 

注意：
- (Node.js 版本需不低于 10.13，建议使用 Node.js 12.0 及以上版本)
- 使用 Node.js 官方安装程序时，请确保勾选 Add to PATH 选项（默认已勾选）

下载地址：https://nodejs.org/en/download

具体安装步骤：略


## 安装 Git

下载地址：https://git-scm.com/download/

具体安装步骤：略

## 安装 Hexo

```bash
# 设置淘宝源
npm config set registry https://registry.npmmirror.com
# 安装 Hexo
npm install -g hexo-cli
```

## 使用 Hexo

```bash
hexo init hexo-pages
cd hexo-pages
npm install
hexo server
```

在 `source\_post` 文件下，编写 markdown 文档即可，文件名称推荐使用简单的英文表示。

如果有图片等资源，可以放在 `source/images` 下，使用`![](/images/image.jpg)` 的方法访问它们。

## 部署 hexo

在 GitHub Pages 部署 Hexo


或者使用以下自动化方法部署：

1、安装 hexo-deployer-git

```bash
npm install hexo-deployer-git --save
```

2、修改 `_config.yml` 配置文件

```yaml
deploy:
  type: git
  repo: https://github.com/<username>/<project>
  # example, https://github.com/hexojs/hexojs.github.io
  branch: main
```

记得修改 `_config.yml` 为你的真实域名：https://username.github.io/project

3、执行 `hexo clean && hexo deploy` 。

4、浏览 `<GitHub 用户名>.github.io` 检查你的网站能否运作。