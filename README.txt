没啥用 · 部署包
================

这个文件夹就是完整站点，必须把 index.html 和 vendor/ 一起上传，缺一不可。

一、Netlify Drop（最快，免费）
1. 打开 https://app.netlify.com/drop
2. 把这个文件夹整个拖进去
3. 得到一个 https://xxx.netlify.app 永久地址
4. 手机上直接打开即可，任何网络都行

二、Vercel（免费）
1. https://vercel.com/new  → 选择上传文件夹
2. 框架选 Other，直接 Deploy

三、GitHub Pages（免费）
1. 新建仓库，上传本文件夹全部内容
2. Settings → Pages → Branch: main / root → Save
3. 得到 https://用户名.github.io/仓库名/

四、Cloudflare Pages（免费）
1. https://dash.cloudflare.com → Pages → Upload assets
2. 上传本文件夹

注意
- 必须保留 vendor/ 目录（OCR 引擎与中文语言包）。
- netlify.toml / vercel.json / _headers 已配置好：index.html 不缓存，vendor 长缓存，避免旧页面导致识别失败。
- 部署后地址固定，不再依赖电脑开机。
