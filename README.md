# Blender Gaussian Quick Viewer (3DGS / 4DGS)
![Banner Recommendation](asset/Banner_Corgi.png)

A lightweight Gaussian data visualization node for Blender

📘 Overview | 简介

A custom Blender node originally developed by Mediastorm during the ASUS 4DGS Yungang Grottoes project.
It supports loading and previewing of 3D Gaussian Splatting (3DGS) and 4D Gaussian Splatting (4DGS) datasets,

providing basic visualization styles for quick inspection and camera motion design.
This viewer represents an early component of the Universal Gaussian Rendering System (UGRS),
a broader R&D effort exploring unified Gaussian rendering and visualization workflows.

Its technology was later featured in the SIGGRAPH 2025 Real-Time Live! showcase
“InfiniteStudio: 4D Volumetric Capture for Filmmaking and Beyond” —
which received the Best in Show Award.

The Blender demo from that showcase has since been officially included in the Blender Demo Files collection:

👉 Blender Demo File – Blender Real-time 4D Gaussian Splatting Demo (coming soon)

👉 Details Page – [Blender Real-time 4D Gaussian Splatting](https://mediastorm.feishu.cn/wiki/FX4uwBlbci141PkyuqYcGbNInpe?from=from_copylink)

👉 4DGS dataset(example scenes) - [download](https://pan.baidu.com/s/1pYY0hi6xXo2q32mOzjXqJQ?pwd=ncdd)

---

🧩 Features

✅ Load and visualize .ply files for 3DGS and 4DGS
✅ Basic shader presets for stylized or analytic previews
✅ Easy to integrate into custom Blender pipelines
🧪 Experimental visualization for dynamic 4DGS sequences

---

🔧 Requirements

Blender 4.3+

Platform: Windows / macOS / Linux

---

## 🚀 How to Use
1. Clone or download this repository.
   
[![Preview](asset/M0.jpg)]()


2. Add the provided assets into your Blender scene collection.（The sample project already includes a 4D corgi .ply asset.）
   
[![Preview](asset/M1.jpg)]()

3. Create a new collection to store seq05 and exclude it from rendering visibility.
   
[![Preview](asset/M2.jpg)]()

4. If using a new project:
   Go to File → Append → NodeTree → GeometryNodesTree
   Add the node group in the Geometry Nodes editor via Add (Shift + A) → Group → GeometryNodesTree

5. Load the 3DGS/4DGS .ply file through the node’s file path input, and ensure the parameters match the reference setup.
   
[![Preview](asset/M3.jpg)]()

6. Control playback via the Frame_Index_input parameter. You can keyframe it manually or enter #frame to bind it to the current timeline frame.
   
[![Preview](asset/M4.jpg)]()

⚠️ Important:
If your 4DGS .ply file contains an attribute named t, rename it to ttt before import —
Blender silently ignores attributes named t due to internal parsing rules.

---

🧱 Relation to UGRS

This viewer is part of the Universal Gaussian Rendering System (UGRS) pipeline,
serving as a lightweight, point-based front-end tool for inspecting Gaussian data
before final rendering in external engines.

👉 Explore the Universal Gaussian Rendering System (UGRS):

(Under construction – full system release coming soon)

---

🔬 Technology Exploration

Mediastorm’s ongoing R&D explores advanced Gaussian rendering within Blender’s ecosystem,
bridging procedural rendering, real-time lighting, and volumetric representation.

Current Focus

Spherical Harmonics Shading

[![Preview](asset/eevee_realtime_SH.gif)]()

Full-space Gaussian Evaluation

[![Preview](asset/Path_tracing_4DGS.gif)]()

Realtime Eevee Integration

[![Preview](asset/eevee_realtime_shadow.gif)]()

Shadow & Reflection Support

[![Preview](asset/eevee_realtime_SSR.gif)]()

Proxy Mesh Approximation


---

🙏 Acknowledgements

Special thanks to Zhang Yu (4DV.ai)
for clarifying the fundamental differences between 3DGS and 4DGS in the early stages of development.
His guidance ensured this tool was built on a correct conceptual foundation.

---

## 📺 Follow & Contact

For development logs (in Chinese):
👉 [史莱姆的个人空间（Bilibili）](https://space.bilibili.com/383900492/)

---

## 📄 License

MIT License
