# Gesture Earth 3D 🌍🖐️

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![React](https://img.shields.io/badge/React-19-blue?logo=react)](https://react.dev/)
[![Three.js](https://img.shields.io/badge/Three.js-0.160-black?logo=three.js&logoColor=white)](https://threejs.org/)
[![MediaPipe](https://img.shields.io/badge/MediaPipe-Hands-orange)](https://developers.google.com/mediapipe)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?logo=typescript)](https://www.typescriptlang.org/)

**Gesture Earth**是一个极具未来感的交互式 3D 地球可视化项目。它完全通过摄像头捕捉手势进行控制，无需鼠标或键盘。本项目结合了 **Three.js** 的强大渲染能力和 **Google MediaPipe** 的实时手部追踪技术，构建在现代化的 **React** 应用之上。

![项目预览](https://cdn.jsdelivr.net/gh/czlifetime/img/GestureEarth.png)

## ✨ 功能特性

- **🖐️ 实时手部追踪**：直接在浏览器中检测手部关键点，低延迟，高精度。
- **🌍 沉浸式 3D 地球**：使用 NASA "Blue Marble" 高清纹理进行高保真渲染。
- **🕹️ 直观的手势控制**：
  - **张开手掌 (Open Palm) 🖐️**：平滑放大，查看细节。
  - **握拳 (Fist) ✊**：缩小视角，查看地球全貌。
  - **捏合 (Pinch) 👌**：“选中”区域。将手指向屏幕中心的目标位置（如中国、美国、巴西等），捏合拇指和食指即可识别并高亮显示该国家/地区。
- **⚡ 高性能**：优化的渲染循环，支持硬件加速。

## 🚀 快速开始

### 前置条件

- Node.js (推荐 v16 或更高版本)
- 支持摄像头的现代浏览器 (Chrome, Firefox, Safari, Edge)

### 安装步骤

1. **克隆仓库**
   ```bash
   git clone https://github.com/Cherzing/GestureEarth.git
   cd GesturEarth
   ```

2. **安装依赖**
   *(注意：本项目为了简化演示，主要通过 CDN 加载 MediaPipe 和 Three.js，但仍需安装 React 构建工具依赖)*
   ```bash
   npm install
   ```

3. **运行开发服务器**
   ```bash
   npm run dev
   ```

4. **允许摄像头访问**：在浏览器中打开本地链接（通常是 `http://localhost:5173`），并在提示时允许浏览器访问摄像头。

## 🎮 如何使用

1. **等待初始化**：左上角状态栏会从 "Initializing..."（初始化中）变为显示手势状态。
2. **挥手开始**：确保您的手出现在摄像头视野内。
3. **执行手势**：
   - **导航**：移动手部位置似乎并不直接控制地球旋转（当前版本为自动旋转或基于中心点交互），主要通过手势触发功能。
   - **缩放**：张开五指进行放大，握紧拳头进行缩小。
   - **交互**：将屏幕中心对准想要识别的国家，然后做出“捏合”手势（拇指和食指接触）来确认选择。

## 🛠️ 技术栈

- **前端框架**: React 19 + TypeScript
- **3D 引擎**: Three.js
- **计算机视觉**: MediaPipe Hands (@mediapipe/hands)
- **样式**: Tailwind CSS
- **构建工具**: Vite (推荐用于生产环境)

## 🤝 贡献指南

非常欢迎各种形式的贡献！无论是修复 Bug、改进手势识别逻辑，还是添加更高清的纹理贴图。

1. Fork 本仓库。
2. 创建您的特性分支 (`git checkout -b feature/AmazingFeature`)。
3. 提交您的更改 (`git commit -m 'Add some AmazingFeature'`)。
4. 推送到分支 (`git push origin feature/AmazingFeature`)。
5. 开启一个 Pull Request。

## 📄 许可证

本项目基于 MIT 许可证开源 - 详情请参阅 [LICENSE](LICENSE) 文件。

## 🙏 致谢

- **NASA** 提供开源地球影像数据。
- **Google** 提供强大的 MediaPipe 库。
- **Three.js 社区** 提供无尽的灵感与支持。