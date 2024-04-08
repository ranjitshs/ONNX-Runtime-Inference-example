# ONNX Runtime Inference

## Introduction

ONNX Runtime C++ inference example for image classification using CPU and CUDA.

## Dependencies

* CMake 3.20.1
* ONNX Runtime 1.18.0
* OpenCV 4.9.0

## Usages

### Build Example

```bash
$ cmake -B build
$ cmake --build build --config Release --parallel
```

### Run Example

```bash
$ cd build/src/

# ./inference 
././inference <onnxModelFilePath> <imgFilePath> <labelFilePath>

# ./inference /ranjit/ONNX-Runtime-Inference-main/model/resnet152-v2-7.onnx /ranjit/ONNX-Runtime-Inference-main/data/images/european-bee-eater-2115564_1920.jpg /ranjit/ONNX-Runtime-Inference-main/data/labels/synset.txt 
Model Loading time:1956
Got dynamic batch size. Setting input batch size to 1.
Got dynamic batch size. Setting output batch size to 1.
Number of Input Nodes: 1
Number of Output Nodes: 1
Input Name: data
Input Type: float
Input Dimensions: [1, 3, 224, 224]
Output Name: resnetv27_dense0_fwd
Output Type: float
Output Dimensions: [1, 1000]
Predicted Label ID: 92
Predicted Label: n01828970 bee eater
Uncalibrated Confidence: 0.99903
Minimum Inference Latency: 929.13 ms
```
## References

* [ONNX Runtime C++ Inference](https://leimao.github.io/blog/ONNX-Runtime-CPP-Inference/)
* [ONNX Modes](https://github.com/onnx/models/)
