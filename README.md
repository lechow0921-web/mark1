# 王乐舟 Lezhou Wang · 个人网站 v3

线上地址：（待部署后填写）

这是基于 2026.10 新版简历（品牌传播与内容创作方向）的新网站。它和旧网站 https://lechow0921-web.github.io/make-it-public/ 互相独立，部署本网站时不要动旧仓库。

纯静态网站，所有文件平铺在仓库根目录（index.html 和 15 张 .webp 照片放在一起），没有子文件夹，上传时不会出现路径错位。

## 首次部署

1. 在 GitHub 新建一个 **Public** 仓库，例如 `lezhou-v3`。
2. 进入仓库，点 **Add file → Upload files**，把本文件夹里的 `index.html` 和全部 `.webp` 文件拖进去（README.md 可传可不传），点 **Commit changes**。
3. 打开仓库的 **Settings → Pages**，在 Source 处选 **Deploy from a branch**，分支选 `main`、目录选 `/ (root)`，点 **Save**。
4. 等 1–2 分钟，网站地址为 `https://lechow0921-web.github.io/<仓库名>/`。
5. 拿到地址后，在 `Desktop/cv/site-v3/` 运行 `node deploy.js https://lechow0921-web.github.io/<仓库名>/`，再把新生成的 `index.html` 上传覆盖一次。这样微信和 LinkedIn 分享时才能显示封面图。

## 更新网站

1. 在 `Desktop/cv/site-v3/` 编辑 `layout.html`（结构与样式）和 `app.js.html`（脚本）。
2. 依次运行 `node build.js` 和 `node deploy.js <网站地址>`，新版本会自动写入本文件夹。
3. 在新仓库点 **Add file → Upload files**，把改动过的文件拖进去，点 **Commit changes**，同名文件会被直接覆盖。
4. 等 1–2 分钟，按 Ctrl+F5 强制刷新网页。

## 说明

- **AI 原型在公开网站上运行于检索模式**：“问问 AI 版的我”按关键词返回预先写好的回答，术语翻译回放示例。实时生成只在 Claude 的 Artifact 页面里可用。
- **字体**从 Google Fonts 加载；在国内网络下可能较慢或加载不到，页面会自动退回苹方 / 微软雅黑。
- **隐私**：网站只公开邮箱，不放手机号。
