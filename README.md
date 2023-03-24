# [Data Setting for YOLOv5](https://github.com/Team-BoonMoSa/MakeData)

```shell
Paraent/datasets/MakeData$ python saveData.py
100%|████████████████████████████████████████████████████████████████████████| 2235/2235 [00:45<00:00, 49.47it/s]
==============================
No. Total Data:  2235
==============================
Training Data: No. Images 1861
Training Data: No. GT 1861
Validation Data: No. Images 187
Validation Data: No. GT 187
Test Data: No. Images 187
Test Data: No. GT 187
==============================
No. Total Image Data:  2235
No. Total GT Data:  2235
==============================
```

# Train

```shell
Paraent/YOLOv5$ python segment/train.py --data LogoRec.yaml --epochs 500 --weights yolov5${모델 버전}-seg.pt --batch-size 32
```

# Test

> 모자이크 없는 결과 출력

```shell
Paraent/YOLOv5$ python segment/predict.py --weights runs/train-seg/${훈련된 가중치}/weights/best.pt --source ../datasets/LogoRec/images/test --bms 0
```

> 모자이크 있는 결과 출력

```shell
Paraent/YOLOv5$ python segment/predict.py --weights runs/train-seg/${훈련된 가중치}/weights/best.pt --source ../datasets/LogoRec/images/test --bms 1
```

> :tada: Demo! :tada:

```shell
Paraent/YOLOv5$ python segment/predict.py --weights runs/train-seg/${훈련된 가중치}/weights/best.pt --source ../datasets/LogoRec/images/test --bms 2
```