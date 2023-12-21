# Machine-Learning
The Machine Learning part of this project is creating a machine learning model that can identify artifact images. In this feature, users can scan artifacts using their cellphone camera and then the model will recognize the image. The output from the model is then used by the application system to provide information about the artifact.

## Artifact Image Identifier
The artifact image identifier model was created using the TensorFlow library with a Convolutional Neural Network (CNN) architecture. This model was created to recognize artifact images scanned by the user. We create the model with the following architecture:
- Conv2D(32, (3,3), 'relu', (224,224,3))
- MaxPooling2D(2,2)
- Conv2D(64, (3,3), 'relu', (224,224,3))
- MaxPooling2D(2,2)
- Conv2D(128, (3,3), 'relu', (224,224,3))
- MaxPooling2D(2,2)
- Flatten()
- Dense(256, 'relu')
- Dense(1, 'sigmoid')

The dataset we used to train the model was collected manually and stored on the Google Drive platform: [Artifact Images Dataset](https://drive.google.com/drive/folders/17DuZVnSX4-Urku10jKksakwu7I4FoNNn?usp=sharing). The dataset consists of 1,800 artifact images in .jpg format which are divided into two classes, namely Chinese Ceramics and Pis Bolong. For the model training process, we split the dataset by 70% for training data and 30% for validation data.
