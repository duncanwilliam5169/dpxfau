安信归一平台地址【Q-——333307——】安信归一平台地址【 辋芷《888yx●vip》 】
安信归一平台地址【Q-——333307——】安信归一平台地址【 辋芷《888yx●vip》 】

 从0到1搭建个人技术博客：我是如何用Github Pages + Hexo实现自动化部署的

> 你是否也曾在本地写好了技术文章，却因为部署流程繁琐而放弃更新？这篇文章分享我基于Github Pages和Hexo搭建博客的完整方案，并实现一键自动化部署，希望对你有帮助。

 为什么选择Hexo + Github Pages？

在对比了WordPress、VuePress、Docusaurus等方案后，我最终选择了 Hexo + Github Pages 的组合，原因有三：

- 免费且稳定：Github Pages提供无限流量和HTTPS支持，无需购买服务器
- 轻量高效：Hexo基于Node.js，生成静态页面速度极快，SEO友好
- 生态丰富：主题和插件数量庞大，满足个性化需求

 三步完成博客搭建

 第一步：本地环境准备

确保你的电脑已安装Git和Node.js，然后执行：

```bash
npm install -g hexo-cli
hexo init my-blog
cd my-blog
npm install
```

> 小提示：如果网络较慢，可以配置淘宝镜像源加速依赖安装。

 第二步：关联Github仓库

在Github上新建一个名为 `你的用户名.github.io` 的仓库，然后在本地配置SSH密钥并关联远程仓库。

 第三步：实现自动化部署

在博客根目录安装自动部署插件：

```bash
npm install hexo-deployer-git --save
```

修改 `_config.yml` 配置文件：

```yaml
deploy:
  type: git
  repo: git@github.com:你的用户名/你的用户名.github.io.git
  branch: main
```

之后每次写完文章，只需执行：

```bash
hexo clean && hexo g && hexo d
```

三秒内即可完成发布。

 进阶优化：Github Actions持续集成

如果你希望更彻底的“自动化”，可以借助 Github Actions，实现推送代码到仓库时自动构建和部署，连本地命令都省了。

```yaml
 .github/workflows/deploy.yml
name: Deploy to GitHub Pages
on:
  push:
    branches: [master]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with:
          node-version: '18'
      - run: npm install && hexo generate
      - uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./public
```

 你可能会遇到的坑

- 样式丢失：多数是Github Pages的baseURL配置不对，检查 `_config.yml` 中的 `url` 和 `root` 字段
- 部署失败：先确认SSH密钥是否已添加到Github账户，用 `ssh -T git@github.com` 测试
- 图片路径错误：建议使用相对路径引用图片，避免使用CDN绝对路径

 写在最后

搭建博客只是第一步，坚持输出技术沉淀才是关键。我的博客采用这个方案后，写文章-推送-发布 的流程压缩到1分钟内，写作意愿大大提升。

如果你也在纠结技术选型，不妨试试这套方案。你的第一个Github博客部署成功了吗？欢迎在评论区分享你的踩坑经验，或者关注我获取更多前端工程化实战干货。

相关推荐：

https://github.com/garciaandrea162/uovkkl/blob/main/2027%E5%AE%98%E6%96%B9%E7%9B%98%E7%82%B9%EF%BC%9A%E5%AE%89%E4%BF%A1%E5%BD%92%E4%B8%80%E5%9C%B0%E5%9D%80%E5%B9%B3%E5%8F%B0_%E5%8D%B8%E5%85%88%E5%8C%97%E9%97%AD%E7%9D%B9ydqwj.md

<img src="https://i.postimg.cc/DwjQG2Hn/mei-nu-bei-jing-zhao-shang-tu-zhi-zuo-(68).png" />

相关推荐：

https://github.com/garciaandrea162/uovkkl/commit/7b3d9d564feddd698c96ba1a666ca0c00b985aea

<img src="https://i.postimg.cc/DwjQG2Hn/mei-nu-bei-jing-zhao-shang-tu-zhi-zuo-(68).png" />
相关推荐：

https://github.com/carrollduane3403/iavdsm/blob/main/2027%E5%AE%98%E6%96%B9%E6%94%BB%E7%95%A5%EF%BC%9A%E5%AE%89%E4%BF%A1%E5%BD%92%E4%B8%80%E5%9C%B0%E5%9D%80%E6%B5%8B%E9%80%9F_%E7%BA%BA%E5%B2%B8%E7%8B%88%E4%B9%94%E5%88%9Byykrx.md

<img src="https://i.postimg.cc/Hx5bFbx1/mei-nu-bei-jing-zhao-shang-tu-zhi-zuo-(72).png" />
相关推荐：

https://github.com/carrollduane3403/iavdsm/commit/ec111982a8a8e84686ded71f5810625dff0763da

<img src="https://i.postimg.cc/25g4H0CK/mei-nu-bei-jing-zhao-shang-tu-zhi-zuo-(71).png" />

资讯来源：新华网、人民网、央视新闻、中新网、凤凰网、澎湃新闻、界面新闻、新浪新闻、搜狐网、财新网、观察者网、第一财经等主流平台，以独树一帜的观察视角与扎实的深度报道能力，在资讯领域收获广泛关注。
