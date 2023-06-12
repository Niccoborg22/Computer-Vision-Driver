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

## End Result 
--- 
The result of the models can be summarized in this table: 

MODEL | ACCURACY | BEST MODEL
--- | --- | ---
*CNN-ADAM* | 0.8132 | 
*CNN-NADAM* | 0. |
*Transfer-VGG16* | 0. | `YES`
*Transfer-MobileNetV2* | 0. | 

We can conclude that the best model that we have built is **xxx**. From a small testing sample we can also conclude such conclusions: 
**ADD IMAGE TEST**
You can check the final results of each model from the following images:
### CNN-ADAM 
**ADD IMAGES**
### CNN-NADAM 
**ADD IMAGES**
### Transfer-VGG16
**ADD IMAGES**
### Transfer-MobileNetV2
**ADD IMAGES**
