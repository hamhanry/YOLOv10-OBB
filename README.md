# YOLOv10-OBB (Oriented Bounding Box)

As this repo is launched on 10th July, there is still no pretrained model of YOLOv10 that supports OBB, therefore i initiate this repo and perform the training and testing based on [DOTAv1](https://captain-whu.github.io/DOTA/index.html) dataset.

[![Hugging Face Spaces](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue)](https://huggingface.co/spaces/hamhanry/YOLOv10-OBB)

## UPDATES
### 18/07/2024
- converter annotated label studio to YOLO-OBB is done. check the [repo](https://github.com/hamhanry/label-studio-converter-for-YOLO-OBB)

### 14/07/2024
- added pretrained for Yolov10S(1024), Yolov10B, Yolov10L, Yolov10M, Yolov10X.
- wip convertion from Label studio annotation to support training for [YOLO-OBB](https://github.com/hamhanry/label-studio-converter-for-YOLO-OBB)

### 10/07/2024
- added pretrained for Yolov10N and Yolov10S (640)

## FEATURES
- [x] Pretrained YOLOv10-N-OBB
- [x] Pretrained YOLOv10-S-OBB
- [x] Pretrained YOLOv10-M-OBB
- [x] Pretrained YOLOv10-B-OBB
- [x] Pretrained YOLOv10-L-OBB
- [x] Pretrained YOLOv10-X-OBB
- [x] Hugging Face Space (Note: this will regularly updated once the trained model is finished)

## PERFORMANCE
| model | size (pixels) | mAP50 test | mAP50-95 test | Link | Notes |
| ----- | ------------- | --------- | ------------ | ---- | ----- |
|YOLOv10-N-OBB| 1024|0.36|0.235|[Download](https://huggingface.co/spaces/hamhanry/YOLOv10-OBB/blob/main/pretrained/yolov10n-obb.pt)
|YOLOv10-S-OBB| 640|0.394|0.256|[Download](https://huggingface.co/spaces/hamhanry/YOLOv10-OBB/blob/main/pretrained/yolov10s-640-obb.pt) |Coincidentally, this was trained with image size 640 |
|YOLOv10-S-OBB| 1024|0.457|0.312|[Download](https://huggingface.co/spaces/hamhanry/YOLOv10-OBB/blob/main/pretrained/yolov10s-obb.pt) | |
|YOLOv10-M-OBB| 1024|0.496|0.345|[Download](https://huggingface.co/spaces/hamhanry/YOLOv10-OBB/blob/main/pretrained/yolov10m-obb.pt) | |
|YOLOv10-B-OBB| 1024|0.486|0.335|[Download](https://huggingface.co/spaces/hamhanry/YOLOv10-OBB/blob/main/pretrained/yolov10b-obb.pt) | |
|YOLOv10-L-OBB| 1024|0.52|0.369|[Download](https://huggingface.co/spaces/hamhanry/YOLOv10-OBB/blob/main/pretrained/yolov10l-obb.pt) | |
|YOLOv10-X-OBB| 1024|0.527|0.376|[Download](https://huggingface.co/spaces/hamhanry/YOLOv10-OBB/blob/main/pretrained/yolov10x-obb.pt) | |


## INSTALATION
```bash
conda create -n rps python=3.11
conda activate rps
pip install -r requirements.txt
```

## HOW TO USE?
```python
from ultralytics import YOLO

model = YOLO("/path/to/model.pt", task="obb")
model.predict('/path/to/test.jpg', save=True, imgsz=1024, conf=0.5)
```


