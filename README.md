# Driver Behaviour - Computer Vision
## Goal 
--- 
Predict what the driver is doing in each of the picture given
## Technologies
---
The Technologies used in this model are the following: 
- Python
    - Keras
- CNN - Convolusional Neural Network
- Transfer Learning 
- Google Cloud
    - Drive
    - Colab

## Method
---
**All the jupyter notebooks in the repository have been run in Colab**.
In order to achieve the best possible model, two different models have been developed: 
- **CNN Model**: The first model has been developed using a self-built CNN Model
- **Transfer Learning Model**: The second model has been done using Transfer Learning through Keras

Using a pool of driver images, each taken in a car with a driver doing something in the car and categorize each image according to one of the following action: 
- c0: safe driving
- c1: texting - right
- c2: talking on the phone - right
- c3: texting - left
- c4: talking on the phone - left
- c5: operating the radio
- c6: drinking
- c7: reaching behind
- c8: hair and makeup
- c9: talking to passenger

### CNN Model
While developing the CNN Model I have tried to use two different classifiers: 
- **Adam**: Adam optimization is a stochastic gradient descent method that is based on adaptive estimation of first-order and second-order moments.
- **Nadam**: Much like Adam is essentially RMSprop with momentum, Nadam is Adam with Nesterov momentum.

### Transfer Learning Model
While developing the Transfer Learning Model I have tried to use two different trained model: 
- The **VGG16 model** is an image classifier that was trained on the ImageNet dataset. Using the trained model by excluding its top layer and set its input shape to match our image data we will be able to have a model
- The **MobileNetV2** is a lightweight model designed for mobile and embedded vision applications

## Data
---
The data has been retrieved from the following link: https://drive.google.com/file/d/1l1pN5ZQ6gELeWR8H1uZr0V05hP3gfpg_/view?usp=sharing. In order to train the model, the images have been saved in a Google Drive folder following this structure:
- imgs
  - train
    - c0
    - c1
    - c2
    - c3
    - ...
  - test
  - 6imgtest

## Future improvements
---
### Epochs 
Each model has been developed with a single epoch due to time and CPU concerns. In order to get a better model it would be ideal to increase the amount of epochs.
### Learning Rate 
The models have all been trained using a 0.001 learning rate. The LR determines the size of the step at which the optimizer chosen updates the model's weights during the training phase. Choosing an appropriate learning rate often requires experimentation and, given the limits in CPU and time I chose to keep the LR constant in all models. In the future it would be appropriate to experiment and find the best LR to maximize the accuracy.
### Further personalization
At the moment only two different classifiers in the CNN Model and only two trained model in the transfer learning one. As you can see from the results the difference is visible and it could be interesting to try new classifiers and trained model. Some of the ones that should be looked at are the following:
Classifiers: 
- SGD
- RMSprop
- Adadelta
- Adagrad
- Adamax
- Adafactor

Trained model:
- ResNet
- EfficientNet
- Inception-v3


## End Result 
--- 
The result of the models can be summarized in this table: 

MODEL | ACCURACY | BEST MODEL
--- | --- | ---
*CNN-ADAM* | 0.8132 | 
*CNN-NADAM* | 0.8553 |
*Transfer-VGG16* | 0.9301 | `YES`
*Transfer-MobileNetV2* | 0.8935 | 

The final conclusions that we can derive are the following: 
- As a whole, the Transfer learning models are more accurate than the self-built CNN ones
- The difference when using a different classifier or trained model are evident, it would be ideal to perform more test to find a better model
- The best model has been the **Transfer Learning model with the VGG16** trained model


You can check the final results of each model from the following images:
### CNN-ADAM 
**Accuracy**  
![image](https://github.com/Niccoborg22/Computer-Vision-Driver/assets/114749413/f89fa424-ca16-49f3-a9d0-e08471e0f69e)
**Confusion Matrix**  
![image](https://github.com/Niccoborg22/Computer-Vision-Driver/assets/114749413/1cd60067-6dd5-4d4c-b9d0-9e22f48b7bd2)
### CNN-NADAM 
**Accuracy**  
![image](https://github.com/Niccoborg22/Computer-Vision-Driver/assets/114749413/0ca2d83c-04a1-487a-9a47-d404ad405aa4)

**Confusion Matrix**  
![image](https://github.com/Niccoborg22/Computer-Vision-Driver/assets/114749413/15de3e66-9f42-4cc0-b483-a7e5475cdc71)

### Transfer-VGG16
**Accuracy**  
![image](https://github.com/Niccoborg22/Computer-Vision-Driver/assets/114749413/ce261656-03e3-4a53-93e9-006a84d01226)

**Confusion Matrix**  
![image](https://github.com/Niccoborg22/Computer-Vision-Driver/assets/114749413/7974fed5-101c-4fb1-8762-36260b2787a5)

### Transfer-MobileNetV2
**Accuracy**  
![image](https://github.com/Niccoborg22/Computer-Vision-Driver/assets/114749413/e1c6f7ec-2d87-44f8-ab69-f98881231772)

**Confusion Matrix**  
![image](https://github.com/Niccoborg22/Computer-Vision-Driver/assets/114749413/454991d7-3f15-4c92-bbb1-737e8097a0df)


