# Retinal-Image-Classification
We chosen google colab to avoid consuming the time of libraries' installation, just downloading the data in a spesific format:
https://drive.google.com/drive/folders/1I6vKvTMGSPbvKOxqyyDXdAJRIKgsYj0F?usp=sharing
![Screenshot (477)](https://github.com/mernatamerrh19/Retinal-Image-Classification/assets/73619098/d7f042e1-65d7-4fa2-a411-61e258f512e1)

Then preprosessing step:
After resizing all images in (224,224), then normalizing the green channel -only green channel, the other channels may cause loss of data-
then save the preprocessed images in Processed file
![Screenshot (478)](https://github.com/mernatamerrh19/Retinal-Image-Classification/assets/73619098/de1465ee-fc7a-4ce0-84ce-275517563d11)

After that, we extract the features in the .npy files shown using a pre-trained model -ResNet152V2 Model-
library "tensorflow.keras"

from these features, we used the prediction model -SVM- splitting the data to 40% test and 60% train
Specified the kernel to be 'poly' and the regularization parameter C=1.4, also some settings such as; degree=3, gamma='scale', coef0=220.0

Final step we calculated the Evaluation criteria comparing between the predicted labels and the actual ones: Specificity, Accuracy ,Senstivity, F1-Score, AUC 
