# keras-multi-label
keras OpenCV, multilabel neural net, for AWS GPU.


```

LOGIN TO NODE


GPU
$nvidia-smi
    IF NOT AVAILABLE
    1. ls -l /installers
    2. cd installers
    3. sudo ./NVIDIA-Linux-x86_64-375.26.run --silent

$nvidia-smi


SWITCH PYTHON
$workon dl4cv


TRAIN:
$python train.py --dataset dataset --model fashion.model \
        --labelbin mlb.pickle

SCORE:
$python classify.py --model fashion.model --labelbin mlb.pickle --image examples/example_04.jpg

SAMPLE OUTPUT:


2018-05-08 05:28:41.144050: I tensorflow/stream_executor/cuda/cuda_gpu_executor.cc:893] successful NUMA node read from SysFS had negative value (-1), but there must be at least one NUMA node, so returning NUMA node zero
2018-05-08 05:28:41.144573: I tensorflow/core/common_runtime/gpu/gpu_device.cc:955] Found device 0 with properties:
name: Tesla K80
major: 3 minor: 7 memoryClockRate (GHz) 0.8235
pciBusID 0000:00:1e.0
Total memory: 11.17GiB
Free memory: 11.05GiB
2018-05-08 05:28:41.144607: I tensorflow/core/common_runtime/gpu/gpu_device.cc:976] DMA: 0
2018-05-08 05:28:41.144626: I tensorflow/core/common_runtime/gpu/gpu_device.cc:986] 0:   Y
2018-05-08 05:28:41.144651: I tensorflow/core/common_runtime/gpu/gpu_device.cc:1045] Creating TensorFlow device (/gpu:0) -> (device: 0, name: Tesla K80, pci bus id: 0000:00:1e.0)
[INFO] classifying image...
black: 0.02%
blue: 0.00%
dress: 0.00%
jeans: 0.02%
red: 100.00%
shirt: 100.00%

```




source: Thanks to pyimageserach for detailed explanation.
