# simple-page

一个用单个 HTML 文件手写的落地页，通过 **GitHub Pages** 部署。

- 仓库：https://github.com/Opve1/simple-page
- 在线地址：https://opve1.github.io/simple-page/
- 只有两个文件：`index.html`（内联 CSS / JS，零依赖）+ `preview.png`（分享预览图）

## 页面结构

| 区块 | 内容 |
|---|---|
| 顶栏 | 品牌、锚点导航、GitHub、复制网址；滚动后变毛玻璃，顶部有滚动进度条 |
| Hero | 渐变流光大标题、打字机副标题、双按钮、本地时钟、滚动提示 |
| 数字条 | 1 个文件 / 0 依赖 / 100% 静态可托管（进入视口时滚动计数） |
| 特性 | 6 张玻璃卡片，鼠标移入有跟随光斑、边框发亮、整体上浮 |
| 三步 | 写文件 → 推仓库 → 开 Pages |
| 引用 | 一句大字标语 |
| 结尾 CTA | 强调面板 + 仓库链接 + 复制网址 |
| 页脚 | 版权与链接 |

## 效果实现

- 星空画布：原生 canvas，星点随指针被推开、相邻星点自动连线、点击/轻触炸出星火
- 背景：三层极光色块缓慢漂移 + 网格 + 暗角 + 跟随指针的光斑
- 入场：`IntersectionObserver` 触发，元素依次淡入上移；数字滚动计数
- 兼容：手机 / 平板 / 电脑三档断点；`prefers-reduced-motion` 时全部动画降级为静态
- 分享：`og:image` / `twitter:image` 指向 `preview.png`，微信、推特都有预览卡

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
- 推送若连不上 GitHub，先确认本地代理 `http://127.0.0.1:7897` 已开启（`git config http.proxy` 按需设置）。
