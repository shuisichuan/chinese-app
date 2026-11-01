# 中文学习 — 手机版（PWA）

这个文件夹就是可以装到手机上的完整应用：离线可用，有主屏幕图标，全屏打开，进度保存在手机本地。

## 第一步：把文件夹放到网上（任选一种，都免费）

**A. Netlify Drop（最快，约 1 分钟）**
1. 电脑打开 https://app.netlify.com/drop
2. 把整个 `chinese-app-mobile` 文件夹拖进去
3. 得到一个 https 链接，例如 `https://xxxx.netlify.app`

**B. GitHub Pages（长期稳定）**
1. 在 GitHub 新建一个公开仓库，上传本文件夹里的所有文件
2. 仓库 Settings → Pages → Source 选 "Deploy from a branch"，分支选 main、目录选 /(root)
3. 约 1 分钟后得到 `https://用户名.github.io/仓库名/`

## 第二步：装到手机上

- **Android（Chrome）**：打开链接 → 右上角菜单 → "添加到主屏幕 / 安装应用"
- **iPhone（Safari）**：打开链接 → 分享按钮 → "添加到主屏幕"

## Telegram 小程序（Mini App）（俄语用户最常用）
代码已经内置了 Telegram 支持（`index.html` 里的 `TG` 部分），不需要机器人服务器，只要：
1. 先完成第一步，拿到 **https** 链接（Telegram 只接受 https）
2. 在 Telegram 里找 @BotFather，发送 `/newbot` 创建机器人
3. 发送 `/newapp`，选刚建的机器人，Web App URL 填第一步得到的链接
   - 想让机器人聊天框左下角出现“打开”按钮：`/mybots` → 选机器人 → Bot Settings → Menu Button → 填同一个链接
4. 用户点开机器人链接 `https://t.me/机器人名/短名`，就能在 Telegram 里直接学习

在 Telegram 里会自动启用：
- 全高度展开、禁用下滑关闭（避免滚动时误关）
- 跟随 Telegram 的深色/浅色主题，顶部/底部栏同色
- Telegram 自带的返回按钮（课程中返回、子页面返回主页）；课程中关闭会弹出确认
- 答题震动反馈；个人页显示 Telegram 名字
- 学习进度同步到 Telegram 云端（CloudStorage），换手机/电脑登录同一账号进度还在

## 内容
- 词汇：HSK 1、HSK 2 全部，加上 HSK 3 的第一部分（共 635 词），每个词都有例句和造句练习
- 「Практика」标签页（原“Повтор”）：
  - Прописи：只练已经学过的词里的汉字，按笔画从少到多排序（Hanzi Writer 笔顺描写）。单词页每个词旁边的铅笔按钮也能进入。首次使用需要联网，数据来自 cdn.jsdelivr.net，之后会被缓存
  - Пиньинь：拼音参考（声调、声母、韵母、拼写规则）加 8 组练习
  - Повторение：弱项词和错题

更新网页后，用户下次打开会自动拿到新版本（`sw.js` 里的缓存版本号每次改动后加 1）。

## 可选：上架应用商店
把第一步的链接填进 https://www.pwabuilder.com ，可生成 Google Play（Android）安装包。
上架 Google Play 需要开发者账号（一次性付费）；iOS App Store 需要 Apple 开发者账号和 Mac。

## 注意
- 发音使用手机自带的中文语音。Android 如果没有声音：设置 → 文字转语音 → 安装中文语音包。
- 学习进度保存在当前手机的浏览器里；换手机或清除浏览器数据会丢失。
