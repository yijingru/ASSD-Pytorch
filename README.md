# ASSD-Pytorch
ASSD learns to highlight useful regions on the feature maps while suppressing the irrelevant information, thereby providing reliable guidance for object detection.

<p align="center">
	<img src="imgs/fig2.png", width="700">
</p>

Please cite the article in your publications if it helps your research:

	@article{YI2019CVIU,
		title = "ASSD: Attentive Single Shot Multibox Detector",
		journal = "Computer Vision and Image Understanding",
		author = "Jingru Yi and Pengxiang Wu and Dimitris N. Metaxas"
	}


| System | VOC2007 test *mAP* | **FPS** (Titan X) | Number of Boxes | Input resolution
|:-------|:-----:|:-------:|:-------:|:-------:|
| [Faster R-CNN (VGG16)](https://github.com/ShaoqingRen/faster_rcnn) | 73.2 | 7 | ~6000 | ~1000 x 600 |
| [YOLO (customized)](http://pjreddie.com/darknet/yolo/) | 63.4 | 45 | 98 | 448 x 448 |
| SSD300 (VGG16) | 77.2 | 46 | 8732 | 300 x 300 |
| SSD512 (VGG16) | 79.8 | 19 | 24564 | 512 x 512 |
| ASSD300 (VGG16) | 80.0 | - | 8732 | 300 x 300 |
| ASSD321 (ResNet101) | 79.5 | 27.5 | 10325 | 321 x 321 |
| ASSD512 (VGG16) | 81.6 | - | 24564 | 512 x 512 |
| ASSD513 (ResNet101) | **83.0** | 16 | 25844 | 513 x 513 |


## Dependencies
Library: OpenCV-Python, PyTorch>0.4.0, Ubuntu 14.04

## Train/Test/Evaluation
Change the mode in main.py, and make changes to config.py, then run
```Shell
python main.py
```
