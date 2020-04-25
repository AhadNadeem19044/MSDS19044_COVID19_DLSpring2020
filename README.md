# MSDS19044_COVID19_DLSpring2020
This repository contains code and results for COVID-19 classification assignment by Deep Learning Spring 2020 course offered at Information Technology University, Lahore, Pakistan. This assignment is only for learning purposes and is not intended to be used for clinical purposes.
## Dataset
https://drive.google.com/drive/u/0/folders/1-FzZhQO9oHIT9SNOWYoKsuz7fe447vtR

## Task 1 (Load pretrained CNN model and fine-tune FC Layers):
In this task we are required to run VGG-16 and ResNet-18 using Pytorch on COVID-19 dataset in order to identify the infected and normal person.
### VGG-16
I have used the following parameters for VGG-16 on COVID19 Dataset:

Epochs = 10
criterion = nn.CrossEntropyLoss()
optimizer = optim.SGD(vgg16.parameters(), lr=0.001, momentum=0.9)

following are the confusion matrices obtained on Training, Validation and testing data:
#### Training:
tensor([[4619.,  300.],
        [ 717., 6318.]])
#### Validation:
tensor([[587.,  28.],
        [110., 775.]])
#### Testing:
tensor([[595.,  20.],
        [ 28., 857.]])

The final accuracy acheived by VGG-16 is 96% which is quite good but it took lot of time even though the convulations are freezed.

## ResNet-18
In case of ResNet-18 following parameters were used:

Epochs = 10
criterion = nn.CrossEntropyLoss()
optimizer = optim.SGD(resnet18.parameters(), lr=0.001, momentum=0.9)

following are the confusion matrices obtained on Training, Validation and testing data:
#### Training:
ttensor([[3928.,  991.],
        [ 670., 6411.]])

#### Validation:
tensor([[504., 111.],
        [106., 779.]])

#### Testing:
tensor([[538.,  77.],
        [ 58., 827.]])

and the accuracy acheived by ResNet-18 is 91% which is less than VGG-16 in this case but it was far more faster than VGG-16.
