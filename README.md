<img width="363" alt="dog5" src="https://github.com/Eterwait/DogSurf/assets/153010910/d1cfae08-562e-424f-862f-c2ef061b430c">

This repository contains code for training DogSurf - model for surface recontion for robot dog. Repo contains code for preprocessing and training, dataset with five surfaces and weights for different versions of model.  
Name of weights folder contains next information: inner mean, that data was taken fron Unitree Go1 inner sensor, slippery means, that model was trained on general slippery surface, you should collect data from **ice** and **wet_floor** folders together,
standart and PCA means that for this model was used PCA and Standart Scaler preprocessing, \***number**\*h means size of hidden layer, 4 or 5 means number of features after PCA.
Dataset contains data from inner and external IMU sensor.  
Example of data from external sensor:
| Accelerometer X | Accelerometer Y | Accelerometer Z |   Gyroscope X    |   Gyroscope Y    |   Gyroscope Z    |    Not used     |    Not used     |    Not used     |    Not used     |
| :-------------: | :-------------: | :-------------: | :--------------: | :--------------: | :--------------: | :-------------: | :-------------: | :-------------: | :-------------: |
| -10171.0000     | -1005.0000      | 1983.0000       | -6467.0000       | -3533.0000       | 32767.0000       |0.0000           |0.0000           | 0.0000          | 1698491416217   |

In **External data** columns 1-6 are used, in **Inner data** columns 8-13 are used.  
To use code you need create conda inviroment, using **requirements.txt** file and instructions in it.
