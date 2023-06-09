# Face_recognition
Face recognition CNN model based on transfer learning.

# Table of contents
- General Information
- Technologies Used
- Project description
- Project Status
- Contact

# General Information
The project covers all phases of CNN development, from data loading, analysis, model creation, training and evaluation. The project uses transfer learning and the model is based on the ResNet50 model.

# Technologies Used 
  - Python - version 3.9.16,
  - tensorflow - version 2.6.0,
  - numpy - version 1.23.5,
  - matplotlib - version 3.7.0,
  - pandas - version 1.5.3,
  - seaborn - version 0.12.2,
  - scikit-learn - version 1.2.2.

# Project description  
The project includes the following steps: 
- Getting and preprocessing data - used Pins Face Recognition dataset available at https://www.kaggle.com. Train, test, val data sets are loaded from the dataets/ directory using the image data generator, which also enables real-time data augmentation.
- Data visualization and analysis - this step allows to see the data and see how balanced the classes are. 
![image](https://user-images.githubusercontent.com/86266104/225667993-e44a3235-843a-40ec-bb7e-4c3393cdd81c.png)
![image](https://user-images.githubusercontent.com/86266104/225668425-ca7a5049-b418-4e53-86a2-87655591e669.png)
![image](https://user-images.githubusercontent.com/86266104/225727224-c6a2d55d-3106-4098-b904-5f5fa2068b48.png)
- Creating a model - this step includes the creation of a model. The model is based on the pretrained ResNet50 model with several new layers on the top of this model.
The model was compiled with Adamax optimizer and start learning rate equals to 0.001.

The model architecture before optimization:

![image](https://user-images.githubusercontent.com/86266104/225670562-2820fc32-67e9-43e2-b1a7-0f4eabc434dd.png)

The model architecture after optimization:

![image](https://user-images.githubusercontent.com/86266104/226575962-b9fe780e-ee2c-432d-b9fb-b171a8998cd2.png)

- Training the model - model was traind for 70 epochs with additional reduction of learning rate. The training was done on the GPU unit. 
- Model evaluation - the last step involved checking how the model works on an unknown dataset. The model reached an accuracy of 91.26% on a new dataset. 

Learning curves before optimizaion (very visible overfitting):
![image](https://user-images.githubusercontent.com/86266104/225722076-b38c1316-2946-4ad9-a88f-c9c9c571e8ea.png)

Learning curves after optimizaion:
![image](https://user-images.githubusercontent.com/86266104/226577098-6890a318-bfa6-47f2-af2a-277d426d6419.png)

The model classifies images quite well. Confusion matrices and classification report confirm it.

Confusion matrices before optimizaion:

![image](https://user-images.githubusercontent.com/86266104/225723543-70160035-7012-4496-b5ba-a6f6b637e196.png)

Confusion matrices after optimizaion:
![image](https://user-images.githubusercontent.com/86266104/226578065-693baa12-14bf-4c11-acac-af08d969de98.png)

Classification report before optimizaion:

![image](https://user-images.githubusercontent.com/86266104/225723656-92114ff0-9c77-4337-a541-2906ba69b8b4.png)

Classification report after optimizaion:

![image](https://user-images.githubusercontent.com/86266104/226580424-3bb947b4-3016-458e-bcd9-cf76609e5130.png)

Finally we can see how the model classified new never-before-seen images.

![image](https://user-images.githubusercontent.com/86266104/226580204-b1e6aa58-44c9-433b-882e-a22ec1808942.png)

# Project Status
Optimization. 
	
# Contact
Created by Mateusz Ptak (mateusz.ptak@op.pl, mobile 696 166 418) - feel free to contact me!
