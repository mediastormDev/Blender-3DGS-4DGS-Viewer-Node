# Blender Gaussian Quick Viewer (3DGS / 4DGS)
![Banner Recommendation](asset/Banner_Corgi.png)

A lightweight Gaussian data visualization node for Blender

📘 Overview | 简介

A custom Blender node developed by Mediastorm during the ASUS 4DGS Yungang Grottoes project.
Supports loading and previewing of 3DGS and 4DGS datasets, with basic visualization styles for quick inspection and camera motion design.

由 影视飓风（Mediastorm） 团队在 华硕 4DGS 云冈石窟项目 中开发的 Blender 自定义节点，
支持加载与预览 3D Gaussian Splatting (3DGS) 与 4D Gaussian Splatting (4DGS) 数据，
提供基础渲染样式，用于快速查看与设计运镜。

*4DGS素材下载: https://pan.baidu.com/s/1pYY0hi6xXo2q32mOzjXqJQ?pwd=ncdd

---

🧩 Features | 功能特点

✅ Load and visualize .ply files for 3DGS and 4DGS
✅ Basic shader presets for stylized or analytic previews
✅ Easy to integrate into custom Blender pipelines
🧪 Experimental visualization for dynamic 4DGS sequences

✅ 加载并可视化 .ply 格式的 3DGS / 4DGS 数据
✅ 提供基础着色节点，可用于风格化或调试性预览
✅ 易于集成至自定义 Blender 渲染流程
🧪 支持多段 4DGS 序列的时间动态预览

---

🔧 Requirements | 使用要求

Blender 4.3+（推荐使用 4.5 Alpha 版本以获得更流畅交互体验）

Platform: Windows / macOS / Linux

---

## 🚀 How to Use | 使用方式（以多段4DGS为例）
1. Clone or download this repository. 克隆或下载本仓库
   
[![Preview](asset/M0.jpg)]()


2. Add the provided assets into your Blender scene collection.（The sample project already includes a 4D corgi .ply asset.）
   将资产添加进场景集合（如果是从网盘获取的工程，会自带一个柯基4Dply资产）
   
[![Preview](asset/M1.jpg)]()

4. Create a new collection to store seq0~5 and exclude it from rendering visibility.
   新建一个集合用于存放seq0~5，随后排除该集合
   
[![Preview](asset/M2.jpg)]()

5. If using a new project:
   Go to File → Append → NodeTree → GeometryNodesTree
   Add the node group in the Geometry Nodes editor via Add (Shift + A) → Group → GeometryNodesTree
   如果你开启的是全新的工程或者在项目中使用该节点工具：
   文件-追加-NodeTree-GeometryNodesTree
   随后进入几何节点窗口 - 添加(shift+A) - 群组 - GeometryNodesTree

5. Load the 3DGS/4DGS .ply file through the node’s file path input, and ensure the parameters match the reference setup.
   使用节点读取包含 3DGS / 4DGS 数据的 `.ply` 文件，检查设置是否与图中一致
   
[![Preview](asset/M3.jpg)]()

6. Control playback via the Frame_Index_input parameter. You can keyframe it manually or enter #frame to bind it to the current timeline frame.
   Frame_Index_input参数指定了当前的时刻，你可以给他k关键帧，或者直接输入“#frame”指定一个驱动器
   
[![Preview](asset/M4.jpg)]()

⚠️ Important:
If your 4DGS .ply file contains an attribute named t, rename it to ttt before import —
Blender silently ignores attributes named t due to internal parsing rules.
若你的 4DGS .ply 文件中包含属性 t，请在导入前重命名为 ttt，
因为 Blender 内部命名解析机制会忽略该属性，导致动画信息无法识别。

---

🧱 Relation to UGRS | 与 UGRS 的关系

This viewer is part of the Universal Gaussian Rendering System (UGRS) pipeline,
serving as a lightweight, point-based front-end tool for inspecting Gaussian data
before final rendering in external engines.

本节点是 UGRS 通用高斯渲染系统 的一部分，
定位为 轻量级前端工具，用于快速预览高斯数据与设计运镜，
随后可将场景导出至外部高斯渲染器中完成最终合成。

👉 Explore UGRS (Under construction): Universal Gaussian Rendering System
👉 Blender Gaussian Quick Viewer: (This repository)
A lightweight visualization tool for pre-rendering workflow.

---

## 🚀 Technology Exploration | 技术探索方向

🔬 Technology Exploration | 技术探索方向

Mediastorm’s ongoing R&D explores advanced Gaussian rendering within Blender’s ecosystem,
bridging procedural rendering, real-time lighting, and volumetric representation.

影视飓风持续探索 Blender 实时高斯渲染管线，
研究方向包括程序化渲染、实时光照与体渲染一体化。

Current Focus | 研究重点：

Spherical Harmonics Shading | 球谐方向性着色

[![Preview](asset/eevee_realtime_SH.gif)]()

Full-space Gaussian Evaluation | 全空间高斯响应评估

[![Preview](asset/Path_tracing_4DGS.gif)]()

Realtime Eevee Integration | 实时 Eevee 预览优化

[![Preview](asset/eevee_realtime_shadow.gif)]()

Shadow & Reflection Support | 阴影与反射交互

[![Preview](asset/eevee_realtime_SSR.gif)]()

Proxy Mesh Approximation | 代理几何优化


---

🙏 Acknowledgements | 致谢

Special thanks to Zhang Yu (4DV.ai)
for clarifying the fundamental differences between 3DGS and 4DGS in the early stages of development.
His guidance ensured this tool was built on a correct conceptual foundation.

特别感谢来自 视维智能 4DV.ai 的 张宇，
在项目初期帮助我们深入理解 3DGS 与 4DGS 的技术差异，
否则我们可能一直以为“4DGS只是多个3DGS串起来”。🙂

---

## 📺 Follow & Contact | 关注与联系

For development logs (in Chinese):
如需了解更多开发动态与学习内容（中文更新）：
👉 [史莱姆的个人空间（Bilibili）](https://space.bilibili.com/383900492/)

---

## 📄 License | 许可协议

MIT License / MIT 开源协议
