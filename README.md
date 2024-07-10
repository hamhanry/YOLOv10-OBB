# YOLOv10-OBB (Oriented Bounding Box)

As this repo is launched on 10th July, there is still no pretrained model of YOLOv10 that supports OBB, therefore i initiate this repo and perform the training and testing based on [DOTAv1](https://captain-whu.github.io/DOTA/index.html) dataset.

## FEATURES
- [ ] Pretrained YOLOv10-N-OBB
- [ ] Pretrained YOLOv10-S-OBB
- [ ] Pretrained YOLOv10-M-OBB
- [ ] Pretrained YOLOv10-B-OBB
- [ ] Pretrained YOLOv10-L-OBB
- [ ] Pretrained YOLOv10-X-OBB
- [ ] Hugging Face Space

## PERFORMANCE
| model | size (pixels) | mAP50 val | mAP50-95 val | FLOPs (B) | Link |
| ----- | ------------- | --------- | ------------ | --------- | ---- |
|YOLOv10-N-OBB| 1024|  |  |  | [TBA]()
|YOLOv10-S-OBB| 1024|  |  |  | [TBA]()
|YOLOv10-M-OBB| 1024|  |  |  | [TBA]()
|YOLOv10-B-OBB| 1024|  |  |  | [TBA]()
|YOLOv10-L-OBB| 1024|  |  |  | [TBA]()
|YOLOv10-X-OBB| 1024|  |  |  | [TBA]()


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


