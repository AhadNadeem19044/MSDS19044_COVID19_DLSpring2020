## Assignment 5 part 2

### DataSet:
[X-Ray Imbalanced Dataset](https://drive.google.com/drive/folders/1jw9DJ1vzK8CHa28QoKbcDEhqG1U1Slkv?usp=sharing "Dataset Link")

### Task1 (Without Focal Loss):

#### VGG-16:

I have used the following parameters for VGG-16 on COVID19 Dataset:
Loss = BCEWithLogitsLoss
Optimizer = optim.SGD(vgg16.parameters(), lr=0.001, momentum=0.9)

The final accuracy achieved by VGG-16 is **90%** on training set and **96%** for validation set. The loss curve for VGG-16 on Training and Validation data is shown below:

![alt text](https://github.com/AhadNadeem19044/MSDS19044_COVID19_DLSpring2020/blob/master/Part%202/Images/VGG16%20WoFL.png "Vgg16 loss without Focal Loss")
 
#### Confusion Matrix:

##### Training Data:
![alt text](https://github.com/AhadNadeem19044/MSDS19044_COVID19_DLSpring2020/blob/master/Part%202/Images/vgg16%20WoFL%20Train.png "Vgg16 confusion matrix")
 
##### Validation Data:
![alt text](https://github.com/AhadNadeem19044/MSDS19044_COVID19_DLSpring2020/blob/master/Part%202/Images/vgg16%20WoFL%20Validation.png "Vgg16 confusion matrix")
 
#### ResNet-18:
In case of ResNet-18 following parameters were used:

Loss = BCEWithLogitsLoss
Optimizer = optim.SGD(resnet18.parameters(), lr=0.01, momentum=0.9)

The accuracy achieved by ResNet-18 on training set is **85%** and **86%** on validation set, which is less than VGG-16 with these parameters.

The loss curve on train and validation data is shown below:
 ![alt text](https://github.com/AhadNadeem19044/MSDS19044_COVID19_DLSpring2020/blob/master/Part%202/Images/resnet18%20WoFL.png "ResNet-18 loss without Focal Loss")

#### Confusion Matrix:

##### Training Data:
![alt text](https://github.com/AhadNadeem19044/MSDS19044_COVID19_DLSpring2020/blob/master/Part%202/Images/resnet-18%20WoFL%20Train.png "resnet-18 confusion matrix") 

##### Validation Data:
![alt text](https://github.com/AhadNadeem19044/MSDS19044_COVID19_DLSpring2020/blob/master/Part%202/Images/resnet-18%20WoFL%20Validation.png "resnet-18 confusion matrix")
 

### Task 2 (With Focal Loss):


#### ResNet-18:

The parameters used are as follows:
Epochs = 10, optim.SGD(vgg16.parameters(), lr=0.01, momentum=0.9)
Focal loss = Alpha = 0.25, Gamma = 2

The Accuracy achieved by ResNet-18 with focal loss on training data is **82%** and **84%** on validation data, which is low with these parameters.

The loss Curves for Resnet-18 with focal loss is as follows:
![alt text](https://github.com/AhadNadeem19044/MSDS19044_COVID19_DLSpring2020/blob/master/Part%202/Images/resnet18%20WFL.png "ResNet-18 loss with Focal Loss")

#### Confusion Matrix:

##### Training Data:
![alt text](https://github.com/AhadNadeem19044/MSDS19044_COVID19_DLSpring2020/blob/master/Part%202/Images/resnet-18%20WFL%20Train.png "resnet-18 confusion matrix") 
 
##### Validation Data:
![alt text](https://github.com/AhadNadeem19044/MSDS19044_COVID19_DLSpring2020/blob/master/Part%202/Images/resnet-18%20WFL%20Validation.png "resnet-18 confusion matrix") 


#### VGG-16:

The parameters used are as follows:
Epochs = 12, optim.SGD(vgg16.parameters(), lr=0.001, momentum=0.9)
Focal loss = Alpha = 0.25, Gamma = 2

The accuracy achieved by VGG-16 with focal loss on training data is **89%** and **97%** on validation data, which is quite good.

The loss curves for VGG-16 with focal loss is shown below:
![alt text](https://github.com/AhadNadeem19044/MSDS19044_COVID19_DLSpring2020/blob/master/Part%202/Images/vgg16%20WFL.png "Vgg16 loss without Focal Loss")

#### Confusion Matrix:

##### Training Data:
![alt text](https://github.com/AhadNadeem19044/MSDS19044_COVID19_DLSpring2020/blob/master/Part%202/Images/vgg16%20WFL%20Train.png "Vgg16 confusion matrix")

##### Validation Data:
![alt text](https://github.com/AhadNadeem19044/MSDS19044_COVID19_DLSpring2020/blob/master/Part%202/Images/vgg16%20WFL%20Validation.png "Vgg16 confusion matrix")
