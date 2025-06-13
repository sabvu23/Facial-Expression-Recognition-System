# Facial-Expression-Recognition-System

Machines are becoming increasingly integrated into our daily lives. For these systems to 
interact effectively and safely with humans, it is essential that they understand human 
emotions. One of the most natural ways to recognize emotions is through facial 
expressions. However, many current systems lack the capability to accurately interpret 
these expressions in real time.  
To bridge this gap, this project aims to develop a Real-Time Facial Expression 
Recognition (FER) System using Convolutional Neural Networks (CNNs). The system will 
be capable of analyzing facial expressions in real time, enhancing the intuitiveness and 
emotional intelligence of human-computer interactions.

**Dataset Description**

![image](https://github.com/user-attachments/assets/e18bd461-ccb8-4684-928b-bb7f2e24ba70)

Data Source Link: https://www.kaggle.com/datasets/jonathanoheix/face-expression
recognition-dataset  

**Model Architecture Description**

The CNN architecture in this project consist of 4 convolutional layers and 2 fully connected 
layers. The convolutional layer extracts the important features from the images and fully 
connected layers classify the images based on the features extracted.  
The overview of CNN architecture of the project 

![image](https://github.com/user-attachments/assets/6e38b4b0-9141-44f0-93f1-85a3f83d8ca2)

In the first convolutional layer, 64 filters of 3x3 size has been used for extracting basic 
features like edges and textures. BatchNormalization has been defined to normalizing 
activations in order to improve training stability. ReLU function is used as activation 
function to capture non-linear relationship. MaxPooling of size 2x2 is done to reduce 
spatial dimensions, preserving important features and dropout with 0.005 is done for 
preventing from overfitting.  

The second layer has 128 filters of size 5x5 to capture more complex features and others 
remain same as first convolutional layer. 

The third layer has 512 filters of 3x3 size and similar with the fourth layer too.  

The flatten layer converts 2D features maps to 1D feature vectors making it ready for 
connected layers.

The first fully connected layer has 256 neurons (Dense=256) for processing flattened 
features. BatchNormalization has been defined to improve gradient flow. RelU function is 
used as activation function to perform non-linear transformation along with adding 0.05 
dropout value to prevent overfitting.  

The second fully connected layer has 512 neurons for higher representation capacity 
while others are same.  

The final classification layer (output layer) uses softmax activation and produces 
probability distribution cross the 7 classes defined by nb_classes. 

Adam optimization algorithm is used for training neural networks. The Adam optimizer 
object is created with initial learning rate of 0.001.  
The model is then compiled with following parameters: 

1. Optimizer = opt : Uses Adam Optimizer defined earlier 
2. Loss=’categorical_crossentropy’ : specifies loss function for multi-class 
classification where labels are one-hot encoded.  
3. metrics=’accuracy’ : tracking accuracy during training to evaluate model 
performance.

**Accuracy Graph**

![image](https://github.com/user-attachments/assets/5d5f6144-36a7-452a-85f1-8755e1334ab2)


**Loss Graph**

![image](https://github.com/user-attachments/assets/f8426050-77c7-4b7d-927e-3dba4b7c0921)


**Confusion Matrix**

![image](https://github.com/user-attachments/assets/66baaca7-fdc5-4088-afb7-4acf4bebcb73)

****System Interface****

![image](https://github.com/user-attachments/assets/3e1a0f2e-a213-4669-88e7-2ca79af6ca68)

![image](https://github.com/user-attachments/assets/7832c1c5-afe8-4ec3-bd87-c4e0ee1cab2a)




