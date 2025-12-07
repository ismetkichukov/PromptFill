# Concept Art Prompt Generator (概念美术提示词生成器)

一个专为 AI 绘画（GPT、Nano Banana 等）设计的**结构化提示词生成工具**。通过可视化的“填空”交互方式，帮助用户快速构建、管理和迭代复杂的 Prompt。

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/Version-0.2.0-orange.svg)
![React](https://img.shields.io/badge/React-18.x-61DAFB.svg)
![Vite](https://img.shields.io/badge/Vite-5.x-646CFF.svg)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-38B2AC.svg)

## ✨ 核心特性

*   **🧩 智能词库管理**：
    *   **分类管理**：支持自定义词库分类（如人物、动作、画面、物品等），并通过颜色区分，视觉更清晰。
    *   **双向同步**：在右侧预览填空时，可直接添加“自定义选项”，自动反向同步到左侧词库中，无需来回切换。
    *   **分类编辑器**：内置分类管理器，支持增删改分类及其颜色配置（12种预设颜色）。
    *   **响应式布局**：词库列表支持瀑布流式多列布局，空间利用更高效。

*   **📝 多模版系统**：
    *   支持创建多个独立的 Prompt 模版（如“角色概念分解图”、“3x3 摄影网格”）。
    *   **独立状态**：每个模版的变量选择（Selection）互不干扰。
    *   **副本克隆**：支持一键创建模版副本，方便进行 A/B 测试或微调。

*   **🖱️ 可视化交互**：
    *   **所见即所得编辑**：编辑模式下变量根据分类颜色高亮显示，支持直接文本编辑与结构调整。
    *   **拖拽插入**：直接将左侧词库卡片拖入编辑区域，即可快速插入变量。
    *   **预览模式**：模版中的变量（`{{role}}`）会自动渲染为可点击的下拉菜单。
    *   **独立实例**：同一变量在模版中出现多次（如 `{{color}}`），可分别选择不同的值（支持 `color-0`, `color-1` 独立索引）。

*   **💾 自动持久化**：
    *   利用 LocalStorage 自动保存所有修改（模版、词库、分类配置）。
    *   刷新页面或关闭浏览器后，数据不会丢失。

*   **📋 导出与分享**：
    *   **一键复制**：复制最终生成的纯净 Prompt 文本。
    *   **保存长图**：支持将当前填好内容的 Prompt 模版导出为高清图片，方便分享与存档。

## 🛠️ 技术栈

*   **构建工具**: [Vite](https://vitejs.dev/)
*   **前端框架**: [React](https://react.dev/)
*   **样式库**: [Tailwind CSS](https://tailwindcss.com/)
*   **图标库**: [Lucide React](https://lucide.dev/)
*   **导出工具**: [html2canvas](https://html2canvas.hertzen.com/)

## 🚀 快速开始

### 前置要求
确保您的环境已安装 [Node.js](https://nodejs.org/) (推荐 v18+)。

### 安装与运行

1.  **克隆项目**
    ```bash
    git clone https://github.com/TanShilongMario/PromptFill.git
    cd PromptFill
    ```

2.  **安装依赖**
    ```bash
    npm install
    ```

3.  **启动开发服务器**
    ```bash
    npm run dev
    ```
    会自动打开浏览器访问 `http://localhost:5173`。

4.  **构建生产版本**
    ```bash
    npm run build
    ```

### 快捷启动脚本
项目根目录下提供了快捷脚本，双击即可一键启动服务并打开浏览器：
*   **macOS**: `start.command`
*   **Windows**: `start.bat`

## 📖 使用指南

1.  **管理分类 (Categories)**
    *   点击左侧面板顶部的“管理分类”按钮。
    *   在此处您可以添加新分类、修改现有分类名称或颜色，以及删除不需要的分类。

2.  **管理词库 (Banks)**
    *   点击“创建新变量组”添加新的变量词库，并为其指定分类。
    *   在词库卡片中添加具体选项（支持直接输入或批量添加）。

3.  **编辑模版 (Templates)**
    *   点击右上角的“编辑模版”按钮进入可视化编辑模式。
    *   **拖拽插入**：按住左侧的词库卡片，拖入编辑器即可插入变量（如 `{{weather}}`）。
    *   编辑器中的变量会根据其所属分类显示对应颜色，方便识别。

4.  **生成与迭代**
    *   切换回“预览交互”模式。
    *   点击彩色的变量词，选择选项。如果选项不存在，点击下拉菜单底部的“+ 添加自定义选项”，输入并回车即可直接选用并保存。
    *   点击右上角的“复制结果”或“保存长图”。

## 🤝 贡献

欢迎提交 Issue 或 Pull Request 来改进这个项目！

## 📄 许可证

本项目采用 [MIT 许可证](LICENSE)。
