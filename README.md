# 科研网站集合

这是一个可公开分享的静态科研网站导航页。核心页面是 `index.html`，不需要后端、数据库或构建步骤。

## 推荐发布方式：GitHub Pages

1. 在 GitHub 新建一个仓库，例如 `research-sites`。
2. 上传本文件夹中的这些文件：
   - `index.html`
   - `.nojekyll`
   - `网站.txt`
   - `README.md`
3. 打开仓库的 `Settings` -> `Pages`。
4. 在 `Build and deployment` 中选择：
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
5. 保存后等待部署完成，GitHub 会生成一个可分享的网址。

## 其他发布方式

- Netlify：把整个文件夹拖到 Netlify 的站点部署页面即可，`netlify.toml` 已经配置为直接发布当前目录。
- Vercel：导入该文件夹或对应 Git 仓库即可，`vercel.json` 已经配置为静态站点。
- 局域网临时分享：在此目录运行 `python -m http.server 8000`，同一网络中的其他人可访问你的电脑 IP 加端口。

## 更新网站

目前网页中的网站数据写在 `index.html` 的 `sites` 数组中。新增网站时，按下面格式添加一行：

```js
{ name: "网站名称", url: "https://example.com/" }
```

`网站.txt` 保留为原始清单，建议同步维护，格式为：

```txt
网站名称: https://example.com/
```
