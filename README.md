# yolo-train

计算机视觉在农业领域的应用 —— 基于 YOLO 的目标检测项目。

## 项目简介

本项目使用 Ultralytics YOLO 框架，针对农业场景（作物/病虫害/果实等）进行目标检测，包含训练、预测、测试与实时摄像头检测等流程。

## 目录结构

```
yolo-train/
├── README.md                 # 项目说明
├── requirements.txt          # 依赖清单
├── configs/                  # 配置文件（模型/训练参数等）
├── datasets/
│   ├── raw/                  # 原始数据（保持只读）
│   ├── processed/            # 清洗处理后的数据
│   ├── annotations/          # 标注数据
│   └── splits/               # 数据划分（train/val/test）
├── models/
│   ├── losses/               # 自定义损失函数
│   ├── tools/                # 工具函数
│   └── scripts/              # 训练/预测/测试/检测脚本
├── experiments/
│   └── checkpoints/          # 训练权重与日志
└── docs/                     # 文档
```

## 依赖安装

```bash
pip install -r requirements.txt
```

## 使用方法

脚本位于 `models/scripts/` 目录下：

| 脚本 | 用途 |
|------|------|
| `mytrain.py` | 训练模型 |
| `mypredict.py` | 对图片/视频进行预测 |
| `mytest.py` | 测试模型效果 |
| `mycam.py` | 实时摄像头目标检测 |

## 数据说明

原始数据统一存放于 `datasets/raw/`，保持只读；数据清洗、格式转换和数据划分均通过脚本完成，不建议手工修改后只保留最终文件。
