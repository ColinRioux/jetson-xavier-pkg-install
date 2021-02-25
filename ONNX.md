### [< BACK](https://github.com/ColinRioux/jetson-xavier-pkg-install)
# All Things ONNX

## Onnxruntime-gpu
```bash
$ wget https://nvidia.box.com/shared/static/8sc6j25orjcpl6vhq3a4ir8v219fglng.whl \
-O onnxruntime_gpu-1.4.0-cp36-cp36m-linux_aarch64.whl
$ pip install onnxruntime_gpu-1.4.0-cp36-cp36m-linux_aarch64.whl
```
[Source](https://developer.nvidia.com/blog/announcing-onnx-runtime-for-jetson/)


## Onnx Model Zoo
Like PyTorch, Onnx also has a repository of pre-generated onnx models. See [here](https://github.com/onnx/models)

Example:
```bash
$ wget https://github.com/onnx/models/blob/master/vision/object_detection_segmentation/faster-rcnn/model/FasterRCNN-10.onnx?raw=true -O FasterRCNN-10.onnx
```
**Note**: The `raw=true` query is important. This downloads the file in binary as opposed to a text file.
