# Covid19-detection-using-chest-Xray:
Using Convolutional Neural Network, I have implemented a classifier which detects 
whether the person is Normal or infected by other diseases(especially COVID19).

# Dataset
  1) COVID Cases : https://github.com/ieee8023/covid-chestxray-dataset
  2) Normal Cases : https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia
# Basic Model:
   Model: "sequential_6"
_________________________________________________________________
layer     (type)                 Output Shape              Param  
=================================================================
conv2d_7 (Conv2D)            (None, 148, 148, 32)      896       
_________________________________________________________________
conv2d_8 (Conv2D)            (None, 146, 146, 32)      9248      
_________________________________________________________________
max_pooling2d_10 (MaxPooling (None, 73, 73, 32)        0         
_________________________________________________________________
conv2d_9 (Conv2D)            (None, 71, 71, 64)        18496     
_________________________________________________________________
max_pooling2d_11 (MaxPooling (None, 35, 35, 64)        0         
_________________________________________________________________
conv2d_10 (Conv2D)           (None, 33, 33, 128)       73856     
_________________________________________________________________
max_pooling2d_12 (MaxPooling (None, 16, 16, 128)       0         
_________________________________________________________________
flatten_6 (Flatten)          (None, 32768)             0         
_________________________________________________________________
dense_13 (Dense)             (None, 512)               16777728  
_________________________________________________________________
dropout_8 (Dropout)          (None, 512)               0         
_________________________________________________________________
dense_14 (Dense)             (None, 1)                 513       

# Metric Analysis:
  The metrics images folder contains all the training and validation metric images(loss and accuracy).
  
# Directories Arrangement:
        # Train
            >COVID
            >NonCOVID
        # Test
            >COVID
            >NonCOVID
