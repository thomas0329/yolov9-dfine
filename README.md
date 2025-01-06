

``` shell

# train gelan models
torchrun --nproc_per_node 2 --master_port 9527 train.py --workers 8 --device 0,1 --sync-bn --batch 128 --data data/coco.yaml --img 640 --cfg models/detect/gelan-c.yaml --weights 'gelan-c.pt' --name gelan-c --hyp hyp.scratch-high.yaml --min-items 0 --epochs 6 --close-mosaic 15
```

