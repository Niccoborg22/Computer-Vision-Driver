# Driver Behaviour - Computer Vision
### Goal 
--- 
Predict what the driver is doing in each of the picture given
### Technologies
---
The Technologies used in this model are the following: 
- Python
    - Keras
- CNN - Convolusional Neural Network
- Transfer Learning 
- Google Cloud
    - Drive
    - Colab

### Method
---
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

### Data
---
In order to train the model, the images have been saved in a Google Drive folder following this structure:
- imgs
  - train
    - c0
    - c1
    - c2
    - c3
    - ...
  - test

## End Result 
--- 
