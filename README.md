# 🦉 Bubo Reader (Fork)

This is a personal fork of the excellent [Bubo Reader](https://github.com/georgemandis/bubo-rss) by George Mandis. I've made several opinionated changes to the setup, including replacing dependencies with more compact alternatives. Please see the original repository for deployment instructions.

Some changes I made:

* Replace `nunjucks` with `yeahjs`
* Replace `node-fetch` with `httpie`
* Many styling changes, including using the `:target` CSS selector to switch between groups (inspired by https://john-doe.neocities.org/)
* The build script now sorts the feeds in each group by which one has the latest updates (this greatly improves the experience, imo).
* Dark mode via `@media (prefers-color-scheme: dark)`


## 安装

### 第一步：

访问 `https://github.com/kevinfiol/reader`  项目`Fork` 到你自己的仓库。

### 第二步：

如果已经有小伙伴在使用`github搭建博客或者站点`的话可以跳过第二步直接进行第三步操作。

把` fork` 的项目点击设置进行改名字，格式为:` github用户名.github.io`  比如我自己：`xiamuguizhi.github.io`  这样你就可以访问域名` github用户名.github.io`  看到这个页面了。

![](//tp.xiamuyourenzhang.cn/qqmd/QQ截图20211014115556.png)

### 第三步：

ps：直接跳到第三步的小伙伴，可以访问：` github用户名.github.io/reader/`  进行访问。

这时候我们点击`Actions` 动作点击启用作者为我们写好的`自动更新RSS订阅`脚本就可以了，作者默认设置`三十分钟` 执行一次脚本，当然你门可以编辑`github_pages.yml` 修改时间多久更新一次。

![](//tp.xiamuyourenzhang.cn/qqmd/QQ截图20211014120819.png)


### 第四步：

- 点击进入`src` 

![](//tp.xiamuyourenzhang.cn/qqmd/QQ截图20211014115936.png)

- 点击`feeds.json` 文件进入，在点击`右上角` 的`✏` 进行编辑

![](//tp.xiamuyourenzhang.cn/qqmd/QQ截图20211014120107.png)

![](//tp.xiamuyourenzhang.cn/qqmd/QQ截图20211014120248.png)

然后就算对内容进行编辑了，你们可以参考我的，如下：

``` json
{
  "日常生活": [
    "https://xiamuyourenzhang.cn/feed.xml",
    "https://www.linyufan.com/rss.xml",
    "http://gojira.net/feed"
  ],
  "技术博客": [
    "https://zezeshe.com/feed"
  ],
  "blogs": [
    "https://kevinfiol.com/atom.xml"
  ]
}

```

ps： 切记最后一个不需要带` ,  逗号`   ！

最后就是提交保存更新，更新说明随便打什么字都可以，点击绿色按钮`Commit changes` 就能保存更新了。

![](//tp.xiamuyourenzhang.cn/qqmd/QQ截图20211014121314.png)

还记得我们前面第三步设置的自动执行更新脚本吗？除了默认半小时更新一小时外，我们更新一次源文件也能触发一次脚本执行效果，下面我保存提交看看效果吧。

.....

你们看已经在自动更新订阅源了，下面只需要耐心等待博客源更新完毕，然后打开 ` github用户名.github.io` 或者` github用户名.github.io/reader/`   查看你的RSS订阅器吧！

![](//tp.xiamuyourenzhang.cn/qqmd/QQ截图20211014121651.png)
