# [Training Code Follow Up](https://github.com/Team-BoonMoSa/YOLOv5/issues/1)

```shell
python train.py --data coco128.yaml --epochs 300 --weights yolov5m6 --cfg yolov5m.yaml --batch-size 32
```

<details>
<summary>Training Logs</summary>
<div>

```
 Epoch    GPU_mem   box_loss   obj_loss   cls_loss  Instances       Size
  0%|          | 0/4 [00:00<?, ?it/s]train.py:323: FutureWarning: Non-finite norm encountered in torch.nn.utils.clip_grad_norm_; continuing anyway. Note that the default behavior will change in a future release to error out if a non-finite total norm is encountered. At that point, setting error_if_nonfinite=false will be required to retain the old behavior.
  torch.nn.utils.clip_grad_norm_(model.parameters(), max_norm=10.0)  # clip gradients
      0/299      2.51G       0.11    0.06781      0.106        455        640: 100%|██████████| 4/4 [00:40<00:00, 10.13s/it]
                 Class     Images  Instances          P          R      mAP50   mAP50-95: 100%|██████████| 2/2 [00:00<00:00,  4.67it/s]
                   all        128        929          0          0          0          0

      Epoch    GPU_mem   box_loss   obj_loss   cls_loss  Instances       Size
      1/299      6.11G     0.1099    0.07716     0.1061        380        640: 100%|██████████| 4/4 [00:01<00:00,  2.62it/s]
                 Class     Images  Instances          P          R      mAP50   mAP50-95: 100%|██████████| 2/2 [00:00<00:00,  4.39it/s]
                   all        128        929          0          0          0          0

      Epoch    GPU_mem   box_loss   obj_loss   cls_loss  Instances       Size
      2/299      6.11G     0.1107    0.07112     0.1065        457        640: 100%|██████████| 4/4 [00:01<00:00,  2.63it/s]
                 Class     Images  Instances          P          R      mAP50   mAP50-95: 100%|██████████| 2/2 [00:00<00:00,  4.31it/s]
                   all        128        929          0          0          0          0

      Epoch    GPU_mem   box_loss   obj_loss   cls_loss  Instances       Size
      3/299      6.11G     0.1098    0.08129     0.1063        452        640: 100%|██████████| 4/4 [00:01<00:00,  2.62it/s]
                 Class     Images  Instances          P          R      mAP50   mAP50-95: 100%|██████████| 2/2 [00:00<00:00,  4.50it/s]
                   all        128        929          0          0          0          0

      Epoch    GPU_mem   box_loss   obj_loss   cls_loss  Instances       Size
      4/299      6.11G     0.1091     0.0742     0.1061        385        640: 100%|██████████| 4/4 [00:01<00:00,  2.85it/s]
                 Class     Images  Instances          P          R      mAP50   mAP50-95: 100%|██████████| 2/2 [00:00<00:00,  4.24it/s]
                   all        128        929          0          0          0          0

      Epoch    GPU_mem   box_loss   obj_loss   cls_loss  Instances       Size
      5/299      6.11G     0.1091    0.07433     0.1059        452        640: 100%|██████████| 4/4 [00:01<00:00,  2.79it/s]
                 Class     Images  Instances          P          R      mAP50   mAP50-95: 100%|██████████| 2/2 [00:00<00:00,  4.46it/s]
                   all        128        929          0          0          0          0

      Epoch    GPU_mem   box_loss   obj_loss   cls_loss  Instances       Size
      6/299      6.11G      0.108     0.0719      0.105        449        640: 100%|██████████| 4/4 [00:01<00:00,  2.57it/s]
                 Class     Images  Instances          P          R      mAP50   mAP50-95: 100%|██████████| 2/2 [00:00<00:00,  3.87it/s]
                   all        128        929          0          0          0          0

      Epoch    GPU_mem   box_loss   obj_loss   cls_loss  Instances       Size
      7/299      6.11G     0.1066    0.07407     0.1049        455        640: 100%|██████████| 4/4 [00:01<00:00,  2.65it/s]
                 Class     Images  Instances          P          R      mAP50   mAP50-95: 100%|██████████| 2/2 [00:00<00:00,  4.52it/s]
                   all        128        929          0          0          0          0

      Epoch    GPU_mem   box_loss   obj_loss   cls_loss  Instances       Size
      8/299      6.11G      0.106    0.07617     0.1044        413        640: 100%|██████████| 4/4 [00:01<00:00,  2.58it/s]
                 Class     Images  Instances          P          R      mAP50   mAP50-95: 100%|██████████| 2/2 [00:00<00:00,  4.58it/s]
                   all        128        929          0          0          0          0
```

</div>
</details>

----

# Training for Logo Detection & Segmentation

```shell
python train.py --data FlickrLogos-v2.yaml --epochs 300 --weights yolov5n --cfg yolov5n.yaml --batch-size 32
python segment/train.py --data LogoRec.yaml --epochs 300 --weights yolov5n-seg.pt --batch-size 32
```