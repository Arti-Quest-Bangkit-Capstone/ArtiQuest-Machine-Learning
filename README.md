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

Dataset yang kami gunakan untuk melatih model dikumpulkan secara manual dan disimpan di platform Google Drive: [Artifact Images Dataset](https://drive.google.com/drive/folders/17DuZVnSX4-Urku10jKksakwu7I4FoNNn?usp=sharing). Dataset tersebut terdiri dari 1.800 gambar artefak dengan format .jpg yang dibagi dalam dua kelas yaitu Keramik Cina dan Pis Bolong. Untuk proses pelatihan model, kami melakukan split dataset sebesar 70% untuk training data dan 30% untuk validation data.
