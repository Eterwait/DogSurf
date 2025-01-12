<img width="363" alt="dog5" src="https://github.com/Eterwait/DogSurf/assets/153010910/d1cfae08-562e-424f-862f-c2ef061b430c">

## Welcome to DogSurf!
This repository contains the code for training DogSurf, a model of surface recognition for a robot dog. Repo contains a dataset of five surfaces, preprocessing and training code and weights for different versions of the model.

Folder names contain the following information:  
* *inner*: data was taken from Unitree Go1 inner sensor;
* *slippery*: model was trained on slippery surface, i.e **ice** and **wet_floor** folders together;
* *standard*: Standard Scaler preprocessing was used for this model;
* *PCA*: PCA preprocessing was used for this model;
* ***number*** h: size of a hidden layer;
* *4 or 5*: number of features after PCA.

### Dataset

The dataset contains data from inner and external IMU sensors.
 
**Example of data from external sensor:**
| Accelerometer X | Accelerometer Y | Accelerometer Z |   Gyroscope X    |   Gyroscope Y    |   Gyroscope Z    |    Not used     |    Not used     |    Not used     |    Not used     |
| :-------------: | :-------------: | :-------------: | :--------------: | :--------------: | :--------------: | :-------------: | :-------------: | :-------------: | :-------------: |
| -10171.0000     | -1005.0000      | 1983.0000       | -6467.0000       | -3533.0000       | 32767.0000       |0.0000           |0.0000           | 0.0000          | 1698491416217   |

In **External data** columns 1-6 are used, in **Inner data** columns 8-13 are used.

### Using the code

To use this code, you need to create a Conda environment. Follow the instructions in **requirements.txt**.

### Additional results

Additional performance results of DogSurf, which are not included in the paper, are presented below. They are based on a [QCAT][1] open dataset.   

**Metrics:**
![image_2023-12-08_12-27-49](https://github.com/Eterwait/DogSurf/assets/153010910/d239961d-b129-400e-80cb-3e6fa704bb0b)

**Confusion matrix:**
![image_2023-12-08_12-27-53](https://github.com/Eterwait/DogSurf/assets/153010910/d4f80a7f-1649-4802-ab59-c55b3b1c966e)

[1]: https://www.data.qld.gov.au/dataset/qcat-matters

