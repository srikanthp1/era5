# Image classification

 * we are training our model on MNIST dataset. 
 * we are using a custom convolutional neural network (CNN) architectures. 
 * Implemented in pytorch 

## Info

[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/release/python-370/), 
[PyTorch](https://pytorch.org/), 
[torchvision](https://github.com/pytorch/vision) 0.8, 
Uses [matplotlib](https://matplotlib.org/)  for ploting accuracy and losses.

## Getting Started

To install **PyTorch**, see installation instructions on the [PyTorch website](https://pytorch.org/).

The instructions to install PyTorch should also detail how to install **torchvision** but can also be installed via:

``` bash
pip install torchvision
```


## Usage

```bash
git clone https://github.com/srikanthp1/era5.git
```


## Demo 

[**CustomNetwork**](https://github.com/srikanthp1/era5/blob/main/S5.ipynb) [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/srikanthp1/era5/blob/main/S5.ipynb)

* we have the following:
    * load datasets 
    * augment data
    * define a custom CNN
    * train a model
    * view the outputs of our model
    * visualize the model's representations
    * view the loss and accuracy of the model. 

* **transforms** for trainset and testset are in utils.py. 
* you will also find **dataloaders** in __utils.py__**. 
* **train** and **test** functions are written in __utils.py__**.
* model is written in __model.py__**.
* dataset is downloaded in __S5.ipynb__ file as we may want to try new datasets. 
* transforms if needed to be added or modified refer __utils.py__**.
* visualization of dataset is in __S5.ipynb__**  
* __graphs__** for loss and accuracy is added after training and testing is done


## Model details

```python
model = Net().to(device)
summary(model, input_size=(1, 28, 28))
```

```
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 32, 26, 26]             320
            Conv2d-2           [-1, 64, 24, 24]          18,496
            Conv2d-3          [-1, 128, 10, 10]          73,856
            Conv2d-4            [-1, 256, 8, 8]         295,168
            Linear-5                   [-1, 50]         204,850
            Linear-6                   [-1, 10]             510
================================================================
Total params: 593,200
Trainable params: 593,200
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.67
Params size (MB): 2.26
Estimated Total Size (MB): 2.94
```
