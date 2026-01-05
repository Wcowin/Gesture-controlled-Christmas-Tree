# 🎄 Gesture Christmas Tree

一个用手势控制的 3D 圣诞树互动体验。通过摄像头识别手势，实时控制粒子形态变化，还能上传照片融入圣诞树中。

**Author: Wcowin**


## ✨ 功能

### 🎮 手势交互
| 手势 | 效果 |
|------|------|
| 👊 握 拳 | 粒子聚合成圣诞树 |
| 🖐️ 张开手掌 | 粒子散开飘浮，手势控制旋转 |
| 🤏 捏夹 | 随机聚焦一张照片 |

### 📸 照片功能
- 上传个人照片融入粒子效果
- 照片管理器支持查看/删除
- 照片会随粒子一起运动和旋转

### 🎨 视觉效果
- 1400+ 3D 粒子组成的圣诞树
- 金色、绿色、红色节日配色
- Bloom 后处理光效
- 飘落雪花背景
- 流畅的动画过渡

## 🚀 快速开始

需要通过 HTTP 服务器运行（ES Modules 要求）：

```bash
# Python
python -m http.server 8080

# Node.js
npx serve .

# 或使用 VS Code Live Server
```

访问 `http://localhost:8080`

## 🎯 使用说明

1. 允许浏览器访问摄像头
2. 将手放在摄像头前方
3. 使用不同手势控制圣诞树
4. 按 `H` 键隐藏/显示界面
5. 点击「上传照片」添加个人图片

## 🛠️ 技术栈

- **Three.js** - 3D 渲染引擎
- **MediaPipe** - 手势识别
- **WebGL** - 图形渲染
- **ES Modules** - 模块化

## 📁 项目结构

```
├── index.html              # 主页面（HTML + CSS + JS 一体）
├── README.md               # 说明文档
└── assets/                 # 资源文件
    ├── three.module.js     # Three.js 核心
    ├── EffectComposer.js   # 后处理组合器
    ├── RenderPass.js       # 渲染通道
    ├── UnrealBloomPass.js  # 泛光效果
    ├── Pass.js             # 通道基类
    ├── CopyShader.js       # 复制着色器
    ├── LuminosityHighPassShader.js
    ├── RoomEnvironment.js  # 环境光
    ├── mediapipe-vision.js # MediaPipe 视觉库
    ├── hand_landmarker.task # 手势识别模型
    └── wasm/               # WebAssembly 运行时
```

## ⚙️ 环境要求

- 现代浏览器（Chrome/Edge/Safari）
- WebGL 2.0 支持
- 摄像头权限
- HTTPS 或 localhost

## 📝 注意事项

- 需要良好光线环境以提高手势识别准确度
- 移动端体验可能受限
- 首次加载需要下载手势识别模型

---

Made with ❤️ by **Wcowin**
