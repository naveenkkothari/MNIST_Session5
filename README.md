Mnist Session 5 
1. Train model with lesss than 20k parameters
2. Achieve accuracy of 99.4%
Final Model
|    Notebook         | Model Parameters | Accuracy (Epoch1) | Description|
|---------------------|-----------------|--------------------|------------|
| MNIST_Session5.ipynb| 19,290 | 99.3% | Final Version|

## Final Model 

    Net(
      (conv1):  nn.Sequential(
            nn.Conv2d(1, 16, 3, padding=1),
            nn.ReLU(),
            nn.BatchNorm2d(16),
            nn.Conv2d(16, 16, 3),
            nn.ReLU(),
            nn.BatchNorm2d(16),
            nn.MaxPool2d(2, 2),
            nn.Dropout(0.25)
        )
      (conv2): nn.Sequential(
            nn.Conv2d(16, 16, 3, padding=1),
            nn.ReLU(),
            nn.BatchNorm2d(16),
            nn.Conv2d(16, 32, 3, padding=1),
            nn.ReLU(),
            nn.BatchNorm2d(32),
            nn.Conv2d(32, 16, 3, stride=2, padding=1),
            nn.ReLU(),
            nn.BatchNorm2d(16),
            nn.MaxPool2d(2, 2),
            nn.Dropout(0.25)
        )
      (conv3): nn.Sequential(
            nn.Conv2d(16, 32, 3, padding=1),
            nn.ReLU(),
            nn.BatchNorm2d(32),
            nn.MaxPool2d(2, 2),
            nn.Dropout(
      (fc1): nn.Sequential(
            nn.Linear(32, 10)
        )

    Model parameters
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 16, 28, 28]             160
              ReLU-2           [-1, 16, 28, 28]               0
       BatchNorm2d-3           [-1, 16, 28, 28]              32
            Conv2d-4           [-1, 16, 26, 26]           2,320
              ReLU-5           [-1, 16, 26, 26]               0
       BatchNorm2d-6           [-1, 16, 26, 26]              32
         MaxPool2d-7           [-1, 16, 13, 13]               0
           Dropout-8           [-1, 16, 13, 13]               0
            Conv2d-9           [-1, 16, 13, 13]           2,320
             ReLU-10           [-1, 16, 13, 13]               0
      BatchNorm2d-11           [-1, 16, 13, 13]              32
           Conv2d-12           [-1, 32, 13, 13]           4,640
             ReLU-13           [-1, 32, 13, 13]               0
      BatchNorm2d-14           [-1, 32, 13, 13]              64
           Conv2d-15             [-1, 16, 7, 7]           4,624
             ReLU-16             [-1, 16, 7, 7]               0
      BatchNorm2d-17             [-1, 16, 7, 7]              32
        MaxPool2d-18             [-1, 16, 3, 3]               0
          Dropout-19             [-1, 16, 3, 3]               0
           Conv2d-20             [-1, 32, 3, 3]           4,640
             ReLU-21             [-1, 32, 3, 3]               0
      BatchNorm2d-22             [-1, 32, 3, 3]              64
        MaxPool2d-23             [-1, 32, 1, 1]               0
          Dropout-24             [-1, 32, 1, 1]               0
           Linear-25                   [-1, 10]             330
================================================================
Total params: 19,290
Trainable params: 19,290
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.79
Params size (MB): 0.07
Estimated Total Size (MB): 0.87
----------------------------------------------------------------

# Training output of 20 epoch
Epoch: 1/20..  Time: 42.39s.. Training Loss: 0.968..  Training Accu: 0.699..  Val Loss: 0.160..  Val Accu: 0.959
Epoch: 2/20..  Time: 41.32s.. Training Loss: 0.261..  Training Accu: 0.928..  Val Loss: 0.080..  Val Accu: 0.976
Epoch: 3/20..  Time: 42.31s.. Training Loss: 0.173..  Training Accu: 0.952..  Val Loss: 0.054..  Val Accu: 0.982
Epoch: 4/20..  Time: 42.38s.. Training Loss: 0.132..  Training Accu: 0.962..  Val Loss: 0.043..  Val Accu: 0.985
Epoch: 5/20..  Time: 41.68s.. Training Loss: 0.110..  Training Accu: 0.969..  Val Loss: 0.043..  Val Accu: 0.986
Validation loss has not improved since: 0.043.. Count:  1
Epoch: 6/20..  Time: 42.57s.. Training Loss: 0.098..  Training Accu: 0.972..  Val Loss: 0.036..  Val Accu: 0.988
Epoch: 7/20..  Time: 41.59s.. Training Loss: 0.088..  Training Accu: 0.975..  Val Loss: 0.035..  Val Accu: 0.988
Epoch: 8/20..  Time: 41.69s.. Training Loss: 0.081..  Training Accu: 0.976..  Val Loss: 0.029..  Val Accu: 0.990
Epoch: 9/20..  Time: 41.79s.. Training Loss: 0.074..  Training Accu: 0.979..  Val Loss: 0.029..  Val Accu: 0.990
Epoch: 10/20..  Time: 42.42s.. Training Loss: 0.068..  Training Accu: 0.981..  Val Loss: 0.028..  Val Accu: 0.991
Epoch: 11/20..  Time: 42.29s.. Training Loss: 0.065..  Training Accu: 0.981..  Val Loss: 0.027..  Val Accu: 0.990
Epoch: 12/20..  Time: 41.32s.. Training Loss: 0.062..  Training Accu: 0.981..  Val Loss: 0.023..  Val Accu: 0.992
Epoch: 13/20..  Time: 41.41s.. Training Loss: 0.059..  Training Accu: 0.983..  Val Loss: 0.025..  Val Accu: 0.992
Validation loss has not improved since: 0.023.. Count:  1
Epoch: 14/20..  Time: 41.77s.. Training Loss: 0.055..  Training Accu: 0.984..  Val Loss: 0.023..  Val Accu: 0.992
Epoch: 15/20..  Time: 41.31s.. Training Loss: 0.052..  Training Accu: 0.984..  Val Loss: 0.024..  Val Accu: 0.992
Validation loss has not improved since: 0.023.. Count:  1
Epoch: 16/20..  Time: 42.86s.. Training Loss: 0.054..  Training Accu: 0.984..  Val Loss: 0.020..  Val Accu: 0.993
Epoch: 17/20..  Time: 41.23s.. Training Loss: 0.050..  Training Accu: 0.985..  Val Loss: 0.022..  Val Accu: 0.993
Validation loss has not improved since: 0.020.. Count:  1
Epoch: 18/20..  Time: 41.22s.. Training Loss: 0.048..  Training Accu: 0.985..  Val Loss: 0.021..  Val Accu: 0.993
Validation loss has not improved since: 0.020.. Count:  2
Epoch: 19/20..  Time: 41.84s.. Training Loss: 0.049..  Training Accu: 0.986..  Val Loss: 0.022..  Val Accu: 0.992
Validation loss has not improved since: 0.020.. Count:  3
Epoch: 20/20..  Time: 41.27s.. Training Loss: 0.048..  Training Accu: 0.986..  Val Loss: 0.021..  Val Accu: 0.993
Validation loss has not improved since: 0.020.. Count:  4

    
