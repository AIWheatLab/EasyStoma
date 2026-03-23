# EasyStoma

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/Deep%20Learning-PyTorch%20%26%20MMSeg-orange)
![PyQt5](https://img.shields.io/badge/GUI-PyQt5-green?logo=qt&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?logo=windows&logoColor=white)

[English](#english) | [中文](#chinese)

---

<a name="english"></a>
## 🔬 EasyStoma: High-Throughput Stomatal Phenotyping Tool

**EasyStoma** is an automated software designed for the high-throughput analysis of plant stomatal phenotypes. It integrates Deep Learning (**MMSegmentation/PyTorch**) for precise segmentation and provides a comprehensive statistical pipeline for morphological and spatial analysis.

> **Note:** This is a closed-source compiled application. We provide a ready-to-use executable for Windows.

### ✨ Key Features

| Feature Category | Description |
| :--- | :--- |
| **🧠 Deep Learning Core** | Integrated **PyTorch** & **OpenMMLab** algorithms for robust segmentation of stomata and pores. |
| **🚀 Batch Processing** | One-click batch analysis for hundreds of images, automatically exporting results to Excel (`.xlsx`). |
| **📏 Phenotyping** | • **Morphological**: Area, Perimeter, Length, Width, Circularity, Eccentricity.<br>• **Functional**: Stomatal Opening Degree, Pore Area, Guard Cell Metrics.<br>• **Population**: Stomatal Density, **SPI** (Stomatal Pore Index). |
| **🌐 Spatial Analysis** | • **Voronoi Diagrams**: Visualization of stomatal distribution homogeneity.<br>• **Topology Network**: Nearest neighbor connections.<br>• **Charts**: Radar & Rose charts for multi-dimensional metric visualization. |
| **🖥️ GUI** | User-friendly interface built with **PyQt5** for visual validation and interaction. |

### 📥 Download

We provide a packaged executable for Windows users. The package includes trained model weights and configuration files.

* **Download Link:** [EasyStoma (Google Drive)](https://drive.google.com/file/d/1erKMNXsbGSvgw0q7cJ549pt9J7HxwnGu/view?usp=drive_link)

### 🚀 Quick Start

1.  **Download & Extract**: Download the zip file from the link above and extract it to a local folder.
2.  **Run Application**: Double-click `EasyStoma.exe` to launch the GUI.
3.  **Workflow**:
    * **Step 1 (Load)**: Click **"1. Open Image Dir"** to select the folder containing your microscopic images.
    * **Step 2 (Settings)**: (Optional) Adjust **"2. Appearance"** or **"3. Pre-processing"** filters (Border/Small object filtering).
    * **Step 3 (Run)**: Click **"4. Batch Analysis"**, select an output directory, and wait for completion.
    * **Step 4 (Visualize)**: Select an image from the bottom list, then use the **"5. Visualization"** dropdown to view Radar, Rose, or Voronoi charts.

---

<br>

---

<a name="chinese"></a>
## 🔬 EasyStoma: 高通量气孔表型分析工具

**EasyStoma** 是一款专为植物气孔表型研究设计的自动化分析软件。它集成了深度学习（**MMSegmentation/PyTorch**）算法以实现高精度分割，并提供了一套完整的形态学与空间分布统计分析流程。

> **注意：** 本软件为闭源桌面应用程序，我们为 Windows 用户提供开箱即用的可执行文件。

### ✨ 主要功能

| 功能类别 | 描述 |
| :--- | :--- |
| **🧠 深度学习内核** | 内置 **PyTorch** & **OpenMMLab** 核心组件，实现气孔与气孔开口的高精度分割。 |
| **🚀 批量处理** | 支持一键处理文件夹内所有图片，自动生成标注图并导出 Excel 数据表 (`.xlsx`)。 |
| **📏 全维度表型** | • **形态指标**: 面积、周长、长/宽、圆度、偏心率等。<br>• **功能指标**: 气孔开口度 (Opening Degree)、保卫细胞面积、气孔开口指数 (SPI)。<br>• **群体指标**: 气孔密度 (Density)、排列一致性。 |
| **🌐 空间拓扑分析** | • **Voronoi 图**: 用于分析气孔分布的均匀性。<br>• **拓扑网络**: 可视化最近邻气孔连接关系。<br>• **图表可视化**: 提供雷达图与玫瑰图，展示多维数据与角度分布。 |
| **🖥️ 图形界面** | 基于 **PyQt5** 构建的交互式界面，支持实时预览与结果验证。 |

### 📥 软件下载

我们提供了打包好的 Windows 可执行程序，下载包中已包含训练好的模型权重和配置文件，无需配置 Python 环境。

* **下载链接:** [EasyStoma (Google Drive)](https://drive.google.com/file/d/1erKMNXsbGSvgw0q7cJ549pt9J7HxwnGu/view?usp=drive_link)

### 🚀 使用教程

1.  **下载与解压**: 点击上方链接下载压缩包，并解压到本地文件夹。
2.  **启动程序**: 双击运行文件夹中的 `EasyStoma.exe`。
3.  **操作流程**:
    * **Step 1 (导入)**: 点击左上角 **"1. Open Image Dir"** 选择包含显微照片的文件夹。
    * **Step 2 (设置)**: (可选) 通过 **"2. Appearance"** 调整颜色，或在 **"3. Pre-processing"** 中勾选过滤选项（过滤边缘/噪点）。
    * **Step 3 (运行)**: 点击 **"4. Batch Analysis"**，选择结果保存路径，程序将自动开始批量处理。
    * **Step 4 (可视化)**: 在底部缩略图栏选择图片，使用 **"5. Visualization"** 下拉菜单实时查看雷达图、玫瑰图或 Voronoi 图。
