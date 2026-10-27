# simple-page

一个非常简单的静态页面，通过 **GitHub Pages** 部署。

- 只有一个文件：`index.html`（内联 CSS / JS，无依赖）
- 托管地址：`https://you-kunpeng.github.io/<仓库名>/`

## 本地预览

直接双击 `index.html`，或在当前目录起一个静态服务：

```bash
python -m http.server 8000
# 打开 http://localhost:8000
```

## 修改

改 `index.html` → 提交推送，GitHub Pages 会自动重新发布（约 1 分钟）。
