# simple-page

一个非常简单的静态页面，通过 **GitHub Pages** 部署。

- 仓库：https://github.com/Opve1/simple-page
- 在线地址：https://opve1.github.io/simple-page/
- 只有两个文件：`index.html`（内联 CSS / JS，零依赖）+ `preview.png`（分享预览图）

## 这个页面有什么

- 星点连线画布：鼠标推开、点击炸出星火（手机轻触同样有效）
- 极光背景 + 网格 + 旋转光晕，卡片玻璃拟态、3D 倾斜跟随鼠标
- 渐变流光标题、打字机副标题、实时时钟、一键复制网址
- 响应式：手机、平板、电脑全适配；`prefers-reduced-motion` 自动降级为静态画面
- 分享到微信/推特有预览卡（`og:image` 指向 `preview.png`）


## 本地预览

直接双击 `index.html`，或在当前目录起一个静态服务：

```bash
python -m http.server 8000
# 打开 http://localhost:8000
```

## 修改后发布

```bash
git add -A
git commit -m "update page"
git push
```

GitHub Pages 会自动重新发布（约 1 分钟）。

## 备注

- Pages 来源：`main` 分支根目录（legacy build），提交推送即触发重建。
- 本机访问 GitHub 需要走本地代理 `http://127.0.0.1:7897`（已写入本仓库的 `http.proxy` 配置）。
