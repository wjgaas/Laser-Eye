# Laser Eye : Gaze Estimation via Deep Neural Networks

![BootJump](./asset/logo.webp)

## Installation
### Requirements

* Python 3.5+
* Linux, Windows or macOS
* mxnet (>=1.4)

While not required, for optimal performance(especially for the detector) it is highly recommended to run the code using a CUDA enabled GPU.

### Run

* Prepare an usb camera or some videos
* [Optional] More Accurate Face Alignment
    * Download [Hourglass2(d=3)-CAB pre-trained model](https://github.com/deepinx/deep-face-alignment)
    * Replace `MobileAlignmentorModel` with `CabAlignmentorModel`
* `python3 video_gaze_test.py`


### Tips
* Change `FRAME_SHAPE` in `demo.py` and `draw.py` to edit the processing image size
* Edit`MxnetDetectionModel`'s `scale` parameter to make a suitable input size of face detector
* Use `CabAlignmentorModel('weights/cab2d', 0, gpu=0)` for more powerful face alignment
* More details at [Wiki](https://github.com/1996scarlet/Laser-Eye/wiki)

## Gaze Estimation for MMD Face Capture

<p align="center"><img src="asset/6.gif" /></p>

* Try with [Open Vtuber](https://github.com/1996scarlet/OpenVtuber)


## Face Detection
* [RetinaFace: Single-stage Dense Face Localisation in the Wild](https://arxiv.org/abs/1905.00641)
* [faster-mobile-retinaface (MobileNet Backbone)](https://github.com/1996scarlet/faster-mobile-retinaface)

## Facial Landmarks Detection
* MobileNet-v2 version (1.4MB, using by default)
* [Hourglass2(d=3)-CAB version (37MB)](https://github.com/deepinx/deep-face-alignment)

## Head Pose Estimation
* [head-pose-estimation](https://github.com/lincolnhard/head-pose-estimation)

## Iris Segmentation
* [U-Net version (model size 71KB, TVCG 2019)](https://ieeexplore.ieee.org/document/8818661)

## Other Results
![BootJump](./asset/1.gif)
![BootJump](./asset/3.gif)
![BootJump](./asset/4.gif)
![BootJump](./asset/5.gif)
<!-- ![BootJump](./asset/2.gif) -->

## Citation

```
@article{wang2019realtime,
  title={Realtime and Accurate 3D Eye Gaze Capture with DCNN-based Iris and Pupil Segmentation},
  author={Wang, Zhiyong and Chai, Jinxiang and Xia, Shihong},
  journal={IEEE transactions on visualization and computer graphics},
  year={2019},
  publisher={IEEE}
}

@inproceedings{deng2019retinaface,
title={RetinaFace: Single-stage Dense Face Localisation in the Wild},
author={Deng, Jiankang and Guo, Jia and Yuxiang, Zhou and Jinke Yu and Irene Kotsia and Zafeiriou, Stefanos},
booktitle={arxiv},
year={2019}
}

@inproceedings{Jing2017Stacked,
  title={Stacked Hourglass Network for Robust Facial Landmark Localisation},
  author={Jing, Yang and Liu, Qingshan and Zhang, Kaihua and Jing, Yang and Liu, Qingshan and Zhang, Kaihua and Jing, Yang and Liu, Qingshan and Zhang, Kaihua},
  booktitle={IEEE Conference on Computer Vision & Pattern Recognition Workshops},
  year={2017},
}
```
