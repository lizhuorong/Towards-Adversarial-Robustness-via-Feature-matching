# Towards-Adversarial-Robustness-via-Feature-Matching
This directory contains implementation of an enhanced adversarial training paper as well as models pre-trained on CIFAR-10 and CIFAR-100.
## Pre-requesites

- TensorFlow 1.4 and Python 3.5 

- numpy==1.16.0
## Datasets
Download the dataset which you're going to use and put put them in the corresponding folder.

- [Cifar-10](http://www.cs.toronto.edu/~kriz/cifar-10-python.tar.gz)

- [Cifar-100](http://www.cs.toronto.edu/~kriz/cifar-100-python.tar.gz)

## Overview of the Code
The code consists of Python scripts and the file config.json that contains various parameter settings.
### Running the code
-	python train.py: trains the network, storing checkpoints along the way.
- python eval.py: an infinite evaluation loop, processing each new checkpoint as it is created while logging summaries. It is intended to be run in parallel with the train.py script.
## Parameters in config.json
### Model configuration:
- model_dir: contains the path to the directory of the currently trained/evaluated model.
### Training configuration:
-	random_seed: the seed for the RNG used to initialize the network weights.
-	max_num_training_steps: the number of training steps.
-	num_output_steps: the number of training steps between printing progress in standard output.
-	num_summary_steps: the number of training steps between storing tensorboard summaries.
-	num_checkpoint_steps: the number of training steps between storing model checkpoints.
-	training_batch_size: the size of the training batch.
### Evaluation configuration:
-	num_eval_examples: the number of MNIST examples to evaluate the model on.
-	eval_batch_size: the size of the evaluation batches.
-	eval_on_cpu: forces the eval.py script to run on the CPU so it does not compete with train.py for GPU resources.
### Adversarial examples configuration:
-	epsilon: the maximum allowed perturbation per pixel.
-	k: the number of PGD iterations used by the adversary.
-	a: the size of the PGD adversary steps.
-	random_start: specifies whether the adversary will start iterating from the natural example or a random perturbation of it.
-	loss_func: the loss function used to run pgd on. 
## Pre-trained models
Following set of pre-trained checkpoints released with this code:
|Model|Dataset|Accuracy on clean images|Accuracy on c&w_8_2_30|Accuracy on pgd_8_2_7|Accuracy on pgd_8_2_20|
|:-:|:-:|:-:|:-:|:-:|:-:|
|[wider-ResNet-Cifar10](https://pan.baidu.com/s/1qOa01xfBEbd4Pjkes7rwNw)  (access code:b298)|Cifar-10|85.21%|51.54%|55.74%|52.95%|


|Model|Dataset|Accuracy on clean images|Accuracy on c&w_8_2_10|Accuracy on pgd_8_2_10|Accuracy on pgd_8_2_20|
|:-:|:-:|:-:|:-:|:-:|:-:|
|[wider-ResNet-Cifar100](https://pan.baidu.com/s/1M9yL6oqo7_PXS2JhpnEpKw)  (access code: whoy)|Cifar-100|59.51%|28.00%|31.68%|31.11%|

