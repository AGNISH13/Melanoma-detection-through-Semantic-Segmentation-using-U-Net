# Melanoma-detection-through-Semantic-Segmentation-using-U-Net

## Project Description
This is a python-based project classifying the skin lesion tissue into three different types, based on deep analysis of dermoscopic image samples of the `PH2` dataset through the application of the popular `pre-trained` and `fine-tuned` Convolution Neural Networks,`EfficientNet-b4-widese`, followed by the extraction of deep features from the CNN's `pre-final` layer and consequent classification.

## Dataset description
The PH² dataset has been developed for research and benchmarking purposes, in order to facilitate comparative studies on both segmentation and classification algorithms of dermoscopic images. PH² is a dermoscopic image database acquired at the Dermatology Service of Hospital Pedro Hispano, Matosinhos, Portugal. The dataset is publicly available at:    
https://www.fc.up.pt/addi/ph2%20database.html

## Classes of Division
In this project, we have used the dermoscopic image samples of melanocytic lesions, which have been classified into three categories, namely:  
- `Common Nevus`  
- `Atypical Nevus`
- `Melanoma` 

     
## Flow diagram of the Genetic Algorithm


![image](https://user-images.githubusercontent.com/84792746/154852688-200dd978-ec4a-47c1-b073-0d3249e3d89c.png)


## Dependencies
Since the entire project is based on `Python` programming language, it is necessary to have Python installed in the system. It is recommended to use Python with version `>=3.6`.
The Python packages which are in use in this project are  `matplotlib`, `numpy`, `pandas`, `torch` and `torchvision`. All these dependencies can be installed just by the following command line argument
- pip install `requirements.txt`

## Code implementation
- ### Data paths :
      Current directory -------> segmentation data
                                          |
                                          |
                                          |               
                                          --------------------->  input
                                          |                         |
                                          |             -------------------------
                                          |             |        |              |
                                          |             V        V              V
                                          |           image_1  image_2 ...... image_n
                                          |
                                          |
                                          |              
                                          --------------------->  target
                                                                    |
                                                        -------------------------
                                                        |        |              |
                                                        V        V              V
                                                      image_1  image_2 ...... image_n

      Current directory -------> classification data
                                          |
                                          |
                                          |               
                                          --------------------->  train
                                          |                         |
                                          |             -------------------------
                                          |             |        |              |
                                          |             V        V              V
                                          |           class_1  class_2 ...... class_n
                                          |
                                          |
                                          |              
                                          --------------------->   val
                                                                    |
                                                        -------------------------
                                                        |        |              |
                                                        V        V              V
                                                      class_1  class_2 ...... class_n
                               
- Where the folders `train` and `val` contain the folders of different classes, which include the original dermoscopic images of respective type of skin lesion tissue in `.jpg`/`.png` format for our case.
