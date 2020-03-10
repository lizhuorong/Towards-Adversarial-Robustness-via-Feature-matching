# Towards-Adversarial-Robustness-via-Feature-Matching
This directory contains implementation of an enhanced adversarial training paper as well as models pre-trained on CIFAR-10 and CIFAR-100.
Please contact [CHAO FENG](https://github.com/sqy2012) regarding this code.
## Pre-requesites

- TensorFlow 1.4 and Python 3.5 

- numpy==1.16.0
## Datasets
Download the dataset which you're going to use and put put them in the corresponding folder.

- [Cifar-10](http://www.cs.toronto.edu/~kriz/cifar-10-python.tar.gz)

- [Cifar-100](http://www.cs.toronto.edu/~kriz/cifar-100-python.tar.gz)

## Overview of the Code
The code consists of Python scripts and the file config.json that contains various parameter settings.
### Example usage
-	python train.py: trains the network, storing checkpoints along the way.
- python eval.py: an infinite evaluation loop, processing each new checkpoint as it is created while logging summaries. It is intended to be run in parallel with the train.py script.

## Pre-trained models and Results
Following set of pre-trained checkpoints released with this code:
|Model|Dataset|Accuracy on clean images|Accuracy on c&w_8_2_30|Accuracy on pgd_8_2_7|Accuracy on pgd_8_2_20|
|:-:|:-:|:-:|:-:|:-:|:-:|
|[wider-ResNet-Cifar10](https://pan.baidu.com/s/1qOa01xfBEbd4Pjkes7rwNw)  (access code:b298)|Cifar-10|85.21%|51.54%|55.74%|52.95%|


|Model|Dataset|Accuracy on clean images|Accuracy on c&w_8_2_10|Accuracy on pgd_8_2_10|Accuracy on pgd_8_2_20|
|:-:|:-:|:-:|:-:|:-:|:-:|
|[wider-ResNet-Cifar100](https://pan.baidu.com/s/1M9yL6oqo7_PXS2JhpnEpKw)  (access code: whoy)|Cifar-100|59.51%|28.00%|31.68%|31.11%|

## Acknowledgments
Code referred to the implementation of the [paper](https://arxiv.org/abs/1706.06083).
