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

* **Download Link:** [EasyStoma (Google Drive)](https://drive.google.com/drive/folders/1EcdTy8rvT1d_vgYqoqfyjCyMKH1k7gA4?usp=drive_link)


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

* **下载链接:** [EasyStoma (Google Drive)](https://drive.google.com/drive/folders/1EcdTy8rvT1d_vgYqoqfyjCyMKH1k7gA4?usp=drive_link)

