# 草莓检测项目

## 项目介绍
这是一个基于YOLOv8的草莓成熟度检测系统，支持通过摄像头实时识别草莓的成熟度状态。

## 功能特性
- 实时摄像头草莓检测
- 三种成熟度识别：未成熟、半成熟、全成熟
- 支持图像保存和置信度调整
- 友好的可视化界面

## 环境要求
- Python 3.8+
- OpenCV
- PyTorch
- Ultralytics YOLOv8
- NumPy

## 安装步骤

1. 克隆仓库
```bash
git clone git@github.com:ciyuan1234/yolov8n-.git
cd yolov8n-
```

2. 安装依赖
```bash
pip install opencv-python torch ultralytics numpy
```

3. 运行摄像头识别
```bash
# 方法1：使用虚拟环境（推荐）
.venv\Scripts\python strawberryofcoco\strawberry_camera.py

# 方法2：直接运行
python strawberryofcoco\strawberry_camera.py
```

## 操作说明
- `q` - 退出程序
- `s` - 保存当前帧
- `+` - 增加置信度阈值
- `-` - 减少置信度阈值

## 项目结构
- `strawberryofcoco/` - 主要项目目录
  - `strawberry_camera.py` - 摄像头识别主脚本
  - `runs/` - 训练结果和模型文件
  - `yolo_dataset/` - 数据集配置
  - `test_*.py` - 测试脚本

## 模型说明
项目使用YOLOv8n模型，已训练完成并保存在 `runs/detect/train/weights/best.pt`。

## 注意事项
- 确保摄像头权限已开启
- 首次运行会下载YOLOv8n预训练模型（如果不存在）
- 模型文件较大，请确保网络连接稳定