# EasyStoma

EasyStoma 是一款面向气孔图像的 GPU 分析软件，可执行气孔与气孔孔隙分割、批量分析、Overlay 可视化、表型指标统计及图表输出。

EasyStoma is a GPU-accelerated application for stomatal image segmentation, batch analysis, overlay visualization, phenotypic measurement, and chart generation.

[中文说明](#中文说明) | [English](#english)

---

## 中文说明

### 软件下载

请从以下 Google Drive 链接下载完整软件：

**[Google Drive ]([https://drive.google.com/REPLACE_WITH_YOUR_LINK](https://drive.google.com/drive/folders/1EcdTy8rvT1d_vgYqoqfyjCyMKH1k7gA4?usp=drive_link))**

请下载完整的 `EasyStoma_GPU` 文件夹。不要只下载或复制其中的 `EasyStoma.exe`。

### 系统要求

- Windows 10 或 Windows 11，64 位系统
- 推荐使用支持 CUDA 的 NVIDIA 显卡
- 已正确安装 NVIDIA 显卡驱动
- 至少预留约 5 GB 磁盘空间

软件已经包含 Python、PyTorch、CUDA 运行库及相关依赖，不需要另外安装 Python 或 CUDA Toolkit。

如果没有兼容的 NVIDIA 显卡，软件可能回退到 CPU 推理，但运行速度会明显降低。

### 文件结构

解压后应保持以下结构：

```text
EasyStoma_GPU/
├── EasyStoma.exe
├── README.md
└── _internal/
```

请勿删除、改名或移动 `_internal` 文件夹，也不要把 `EasyStoma.exe` 单独移动到其他位置。

### 启动软件

1. 完整下载并解压 `EasyStoma_GPU`。
2. 双击 `EasyStoma.exe`。
3. 等待界面底部显示 `Model Loaded Successfully.`。
4. 模型加载完成后即可开始分析。

首次启动时，Windows Defender 或 SmartScreen 可能显示安全提示。如果文件来自本项目提供的官方 Google Drive 链接，请确认来源可信后再允许运行。

### 使用方法

1. 点击 **1. Open Image Dir**，选择包含待分析图像的文件夹。
2. 点击底部缩略图选择需要查看的图像。
3. 根据需要设置：
   - **2. Appearance**：调整分割结果的显示颜色。
   - **Filter Border**：过滤接触图像边界的目标。
   - **Filter Small**：过滤较小的噪声区域。
4. 点击 **6. Preview**，对当前图像进行单张预览分析。
5. 点击 **4. Batch Analysis**，选择结果保存目录并开始批量分析。
6. 分析完成后，可通过底部缩略图或左右箭头浏览图像及 Overlay 结果。
7. 使用 **5. Visualization** 查看距离分布、方向玫瑰图、雷达图、拓扑图和 Voronoi 图。

### 支持的图像格式

```text
JPG, JPEG, PNG, TIFF, TIF, BMP
```

输入文件夹可以包含子文件夹，批量输出会尽量保留原有的相对目录结构。

### 批量输出

用户选择的输出目录中会生成：

```text
输出目录/
├── masks/                         分割掩膜
├── overlays/                      原图与分割结果叠加图
├── charts/                        自动生成的分析图表
├── batch_summary.xlsx             批量表型指标汇总
└── batch_mask_diagnostics.xlsx    掩膜像素统计与诊断信息
```

`batch_summary.xlsx` 包含完整的气孔、孔隙、保卫细胞、空间分布和形态学指标。

### 模型说明

- 模型权重和配置已经加密嵌入 `EasyStoma.exe`。
- 软件运行时直接在内存中解密并加载模型。
- 不需要单独下载 `.pth` 或模型配置文件。
- 软件使用 GPU 版本的 PyTorch 进行推理。

### 常见问题

#### 双击后无法启动

- 确认已经完整解压软件。
- 确认 `EasyStoma.exe` 和 `_internal` 位于同一目录。
- 不要直接在压缩包预览窗口中运行 EXE。
- 更新 NVIDIA 显卡驱动后重试。

#### 一直提示模型尚未加载

请等待状态栏显示 `Model Loaded Successfully.` 后再点击预览或批量分析。

#### 推理速度很慢

检查 NVIDIA 显卡驱动是否正常，并在命令提示符中运行以下命令：

```powershell
nvidia-smi
```

如果命令无法识别显卡，软件可能正在使用 CPU 推理。

#### 出现 `torch._C`、DLL 或模块导入错误

通常表示软件文件不完整。请重新下载整个 `EasyStoma_GPU` 文件夹，并确保 `_internal` 中的文件没有被删除或隔离。

#### Overlay 没有显示

请确认模型已经加载完成，并重新点击相应缩略图。批处理完成后，主界面会从批处理输出目录重新载入已保存的 Overlay。

---

## English

### Download

Download the complete application from the following Google Drive link:

**[Google Drive download ]([https://drive.google.com/REPLACE_WITH_YOUR_LINK](https://drive.google.com/drive/folders/1EcdTy8rvT1d_vgYqoqfyjCyMKH1k7gA4?usp=drive_link))**

Download the entire `EasyStoma_GPU` folder. Do not download or copy only `EasyStoma.exe`.

### System requirements

- 64-bit Windows 10 or Windows 11
- An NVIDIA CUDA-capable GPU is recommended
- A working NVIDIA graphics driver
- Approximately 5 GB of free disk space

Python, PyTorch, the CUDA runtime, and the required dependencies are included. Installing Python or the CUDA Toolkit separately is not required.

Without a compatible NVIDIA GPU, the application may fall back to CPU inference, which is considerably slower.

### Folder structure

Keep the following structure after extraction:

```text
EasyStoma_GPU/
├── EasyStoma.exe
├── README.md
└── _internal/
```

Do not delete, rename, or move the `_internal` folder. Do not move `EasyStoma.exe` away from this folder.

### Starting the application

1. Download and fully extract `EasyStoma_GPU`.
2. Double-click `EasyStoma.exe`.
3. Wait until the status bar displays `Model Loaded Successfully.`.
4. Begin the analysis after the model has loaded.

Windows Defender or SmartScreen may display a warning on first launch. Only allow the application to run after confirming that it was downloaded from the official Google Drive link provided by this project.

### Usage

1. Click **1. Open Image Dir** and select the folder containing the input images.
2. Select an image using the thumbnails at the bottom of the window.
3. Configure the optional settings:
   - **2. Appearance**: change the overlay colors.
   - **Filter Border**: remove objects touching the image border.
   - **Filter Small**: remove small noisy regions.
4. Click **6. Preview** to analyze the currently selected image.
5. Click **4. Batch Analysis**, select an output folder, and start batch processing.
6. After processing, use the thumbnails or the left/right buttons to browse the images and their overlays.
7. Use **5. Visualization** to view distance distributions, orientation rose plots, radar charts, topology plots, and Voronoi diagrams.

### Supported image formats

```text
JPG, JPEG, PNG, TIFF, TIF, BMP
```

The input folder may contain subfolders. Batch outputs preserve the relative folder structure where possible.

### Batch outputs

The selected output directory will contain:

```text
Output directory/
├── masks/                         Segmentation masks
├── overlays/                      Original images with segmentation overlays
├── charts/                        Automatically generated charts
├── batch_summary.xlsx             Summary of phenotypic measurements
└── batch_mask_diagnostics.xlsx    Mask pixel counts and diagnostic information
```

`batch_summary.xlsx` contains the complete stomatal, pore, guard-cell, spatial, and morphological measurements.

### Embedded model

- The model weights and configuration are encrypted and embedded in `EasyStoma.exe`.
- They are decrypted and loaded directly in memory at runtime.
- No external `.pth` checkpoint or model configuration file is required.
- Inference uses the GPU-enabled build of PyTorch.

### Troubleshooting

#### The application does not start

- Make sure the package has been fully extracted.
- Make sure `EasyStoma.exe` and `_internal` are in the same folder.
- Do not run the EXE directly from an archive preview window.
- Update the NVIDIA graphics driver and try again.

#### The application says that the model is not loaded

Wait until the status bar displays `Model Loaded Successfully.` before starting a preview or batch analysis.

#### Inference is very slow

Check that the NVIDIA driver is working by running:

```powershell
nvidia-smi
```

If the GPU is not detected, the application may be using CPU inference.

#### A `torch._C`, DLL, or module import error appears

This usually indicates an incomplete package. Download the complete `EasyStoma_GPU` folder again and make sure files inside `_internal` have not been removed or quarantined.

#### The overlay is not displayed

Make sure the model has finished loading, then select the corresponding thumbnail again. After batch processing, the main view can reload the saved overlay from the selected output directory.

---

## Version

EasyStoma V17.9.1 — Windows GPU build

