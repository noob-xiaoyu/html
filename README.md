# GitHub 风格文本对比工具 (GitHub-Style Text Diff Tool)

一个纯前端、零依赖（除了CDN）的网页工具，用于可视化地对比两段文本之间的差异，并以类似 GitHub 的分栏视图高亮显示增、删、改的内容。

---

## ✨ 功能特性

-   **分栏对比视图 (Side-by-Side Diff)**：清晰地在左右两侧展示原始文本和修改后文本。
-   **行级差异高亮**：
    -   <span style="background-color: #e6ffed; color: #22863a;">绿色背景</span> 表示新增的行。
    -   <span style="background-color: #ffeef0; color: #b31d28;">红色背景</span> 表示删除的行。
-   **词级差异高亮 (Intra-line Diff)**：对于被修改的行，能够精确高亮行内发生变化的具体单词或字符。
-   **行号显示**：两侧均显示行号，方便定位。
-   **纯客户端运行**：所有计算都在浏览器中完成，无需后端服务器，保障文本私密性。
-   **响应式设计**：在不同尺寸的屏幕上都有良好的显示效果。

## 🚀 在线体验

**[点击这里进行在线体验](https://noob-xiaoyu.github.io/html/)**

## 🛠️ 技术实现

这个工具完全由前端三剑客构建，并借助了一个强大的开源库：

-   **HTML**: 负责页面结构。
-   **CSS**: 负责所有样式，包括差异高亮的美化。
-   **JavaScript (原生)**: 负责处理用户输入、调用对比算法以及动态生成结果视图。
-   **[jsdiff](https://github.com/kpdecker/jsdiff)**: 核心的差异对比库。本项目通过 CDN 引入，它实现了高效的 `diff` 算法，能够进行行对比和词对比。

## 📖 如何使用

1.  打开 [在线体验链接](https://noob-xiaoyu.github.io/html/)。
2.  在左侧的 “原始文本” 输入框中粘贴你的原始内容。
3.  在右侧的 “修改后文本” 输入框中粘贴修改后的内容。
4.  点击 **“生成对比 (Generate Diff)”** 按钮。
5.  下方的结果区域将立即展示出详细的对比视图。

## 部署到你自己的 GitHub Pages

这个项目是单个 HTML 文件，部署极其简单：

1.  **Fork** 本仓库，或者创建一个你自己的新仓库。
2.  将 `index.html` 文件上传到你的仓库中。
3.  进入仓库的 **Settings** -> **Pages** 页面。
4.  在 **Build and deployment** 部分，将 **Source** 设置为 **Deploy from a branch**。
5.  选择你的主分支（通常是 `main` 或 `master`），文件夹保持 `/(root)`。
6.  点击 **Save**。
7.  等待几分钟，你的文本对比工具就会部署在 `https://noob-xiaoyu.github.io/html/`。

## 📄 许可证

本项目采用 [MIT License](LICENSE) 授权。
