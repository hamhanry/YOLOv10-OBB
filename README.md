# YOLOv10-OBB (Oriented Bounding Box)

As this repo is launched on 10th July, there is still no pretrained model of YOLOv10 that supports OBB, therefore i initiate this repo and perform the training and testing based on [DOTAv1](https://captain-whu.github.io/DOTA/index.html) dataset.

## FEATURES
- [x] Pretrained YOLOv10-N-OBB
- [x] Pretrained YOLOv10-S-OBB
- [ ] Pretrained YOLOv10-M-OBB
- [ ] Pretrained YOLOv10-B-OBB
- [ ] Pretrained YOLOv10-L-OBB
- [ ] Pretrained YOLOv10-X-OBB
- [x] Hugging Face Space (Note: this will regularly updated once the trained model is finished)

## PERFORMANCE
| model | size (pixels) | mAP50 val | mAP50-95 val | Link | Notes |
| ----- | ------------- | --------- | ------------ | ---- | ----- |
|YOLOv10-N-OBB| 1024|0.36|0.235|[Download](https://huggingface.co/spaces/hamhanry/YOLOv10-OBB/blob/main/pretrained/yolov10n-obb.pt)
|YOLOv10-S-OBB| 640|0.394|0.256|[Download](https://huggingface.co/spaces/hamhanry/YOLOv10-OBB/blob/main/pretrained/yolov10s-640-obb.pt) |Coincidentally, this was trained with image size 640 |
|YOLOv10-M-OBB| 1024|  |  | [TBA]() | |
|YOLOv10-B-OBB| 1024|  |  | [TBA]() | |
|YOLOv10-L-OBB| 1024|  |  | [TBA]() | |
|YOLOv10-X-OBB| 1024|  |  | [TBA]() | |


## INSTALATION
```bash
conda create -n rps python=3.11
pip install -r requirements.txt
```

## HOW TO USE?
```python
from ultralytics import YOLO

model = YOLO("/path/to/model.pt", task="obb")
model.predict('/path/to/test.jpg', save=True, imgsz=1024, conf=0.5)
```


