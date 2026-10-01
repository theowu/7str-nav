# Hugo + Cloudflare Pages 导航站 · 手把手部署教程

## 你的菜单结构对照

```
公众号一级菜单          导航站页面
─────────────────────────────────────
娱乐专栏
  ├─ AIGC音乐    →  /aigc-music/
  ├─ AIGC视频    →  /aigc-video/
  ├─ 精品游戏    →  /game/
  └─ 连载小说    →  /novel/

学习空间
  ├─ 魔法教程    →  /tutorial/
  ├─ 法语资讯    →  /french/
  ├─ 财经故事    →  /finance/
  ├─ 认知提升    →  /cognition/
  └─ 指弹吉他    →  /guitar/

魔法工具
  ├─ 开源神器    →  /opensource/
  ├─ 自制神器    →  /homemade/
  └─ 魔法信箱    →  /mailbox/
```

---

## 第1步：安装本地环境（Windows）

### 1.1 安装 Git
1. 下载：https://git-scm.com/download/win
2. 一路下一步安装
3. 验证：右键桌面 → Git Bash Here，输入 `git --version`，看到版本号即成功

### 1.2 安装 Hugo Extended（必须Extended版）
1. 打开 https://github.com/gohugoio/hugo/releases/latest
2. 下载 `hugo_extended_xxx_windows-amd64.zip`
3. 解压到 `C:\hugo\`，里面有 `hugo.exe`
4. 加环境变量：右键「此电脑」→ 属性 → 高级系统设置 → 环境变量 → 系统变量 Path → 编辑 → 新建 → 填 `C:\hugo`
5. 重新打开CMD，输入 `hugo version`，看到版本号即成功

---

## 第2步：本地跑起来

### 2.1 解压项目
把 `guitar-nav-site` 解压到比如 `D:\projects\nav-site`

### 2.2 安装主题
在项目文件夹地址栏输入 `cmd` 回车，然后执行：
```bash
cd D:\projects\nav-site
git init
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

### 2.3 本地预览
```bash
hugo server -D
```
浏览器打开 http://localhost:1313 ，你应该看到导航站首页，上面有3个分类入口。

---

## 第3步：推送到 GitHub

### 3.1 建仓库
1. GitHub 注册并登录
2. 点 New repository，名字随便取如 `my-nav`，选 **Public**，不要勾README，点创建
3. 复制仓库地址，类似 `https://github.com/你的名/my-nav.git`

### 3.2 推送
在项目CMD里执行（替换成你自己的仓库地址）：
```bash
git add .
git commit -m "初始化导航站"
git branch -M main
git remote add origin https://github.com/你的名/my-nav.git
git push -u origin main
```

---

## 第4步：Cloudflare Pages 部署

### 4.1 注册 Cloudflare
打开 https://dash.cloudflare.com/sign-up 注册，免费版即可

### 4.2 创建Pages项目
1. 左侧菜单 → Workers & Pages → Create application → Pages → Connect to Git
2. 授权GitHub，选中你的仓库，点 Begin setup

### 4.3 构建配置（照抄）
| 配置项 | 填什么 |
|--------|--------|
| Project name | 随便取，比如 `my-nav` |
| Production branch | `main` |
| Framework preset | 选 Hugo |
| Build command | `hugo` |
| Build output directory | `public` |

展开 Environment variables (advanced)，加：
| Variable name | Value |
|---------------|-------|
| `HUGO_VERSION` | `0.140.0` |

点 Save and Deploy，等1-2分钟。

成功后你拿到地址：`https://my-nav.pages.dev`，这就是你的导航站！

---

## 第5步：跑通完整链路（发第一篇文章）

### 5.1 公众号发文章
1. 公众号后台 → 草稿箱 → 新建图文
2. 写一篇测试文章，比如「《枫叶城》指弹谱测试」
3. 点 **发布**（不是群发！不推给粉丝）
4. 发布后打开文章，复制浏览器地址栏链接，类似 `https://mp.weixin.qq.com/s/AbC123`

### 5.2 导航站添加这篇文章
1. 打开项目里的 `content/guitar/_index.md`
2. 把示例链接替换成你刚复制的公众号链接：
```markdown
{{< wx_article url="https://mp.weixin.qq.com/s/AbC123" title="《枫叶城》指弹谱" difficulty="★★★" date="2026-10-01" >}}
```
3. 推送：
```bash
git add .
git commit -m "添加《枫叶城》曲谱"
git push
```
4. 等1分钟，打开 `https://my-nav.pages.dev/guitar/`，点卡片 → 跳转公众号文章 ✅

**链路通了！**

---

## 第6步：公众号菜单配置（只配一次，以后不改）

公众号后台 → 自定义菜单，把12个二级菜单全部设置为**跳转网页**，地址如下：

### 一级菜单：娱乐专栏
| 二级菜单 | 跳转地址 |
|----------|----------|
| AIGC音乐 | `https://my-nav.pages.dev/aigc-music/` |
| AIGC视频 | `https://my-nav.pages.dev/aigc-video/` |
| 精品游戏 | `https://my-nav.pages.dev/game/` |
| 连载小说 | `https://my-nav.pages.dev/novel/` |

### 一级菜单：学习空间
| 二级菜单 | 跳转地址 |
|----------|----------|
| 魔法教程 | `https://my-nav.pages.dev/tutorial/` |
| 法语资讯 | `https://my-nav.pages.dev/french/` |
| 财经故事 | `https://my-nav.pages.dev/finance/` |
| 认知提升 | `https://my-nav.pages.dev/cognition/` |
| 指弹吉他 | `https://my-nav.pages.dev/guitar/` |

### 一级菜单：魔法工具
| 二级菜单 | 跳转地址 |
|----------|----------|
| 开源神器 | `https://my-nav.pages.dev/opensource/` |
| 自制神器 | `https://my-nav.pages.dev/homemade/` |
| 魔法信箱 | `https://my-nav.pages.dev/mailbox/` |

保存并发布菜单。**以后再也不用改菜单了！**

---

## 第7步：打通付费闭环

### 7.1 注册面包多
1. 打开 https://mbd.pub 注册并实名认证
2. 发布作品 → 数字商品 → 上传完整版PDF曲谱 → 定价 → 发布
3. 拿到商品链接，类似 `https://mbd.pub/o/XyZ789`

### 7.2 导航站放购买按钮
打开 `content/guitar/_index.md`，在文章列表下面加：
```markdown
{{< buy_button url="https://mbd.pub/o/XyZ789" text="👉 购买完整版曲谱合集" >}}
```
推送代码后，用户点按钮 → 跳转面包多付款 → 自动收PDF ✅

---

## 日常使用流程

### 新增一篇文章
1. 公众号写文章 → 发布 → 复制文章链接
2. 打开对应栏目的 `_index.md`（比如新增曲谱就打开 `content/guitar/_index.md`）
3. 加一行：
```markdown
{{< wx_article url="粘贴公众号链接" title="文章标题" date="2026-10-01" >}}
```
4. 推送：
```bash
git add .
git commit -m "新增：文章标题"
git push
```
5. 1分钟后导航站自动更新 ✅

### 群发推送新内容
公众号群发短图文，底部「阅读原文」填导航站首页地址。

---

## 短代码速查

| 短代码 | 作用 | 示例 |
|--------|------|------|
| `wx_article` | 公众号文章卡片 | `{{< wx_article url="链接" title="标题" difficulty="★★★" >}}` |
| `buy_button` | 购买按钮 | `{{< buy_button url="面包多链接" text="购买" >}}` |
| `bilibili` | B站视频 | `{{< bilibili BV1xx411c7mD >}}` |
| `paywall_notice` | 付费提示框 | `{{< paywall_notice title="付费内容" >}}说明{{< /paywall_notice >}}` |
