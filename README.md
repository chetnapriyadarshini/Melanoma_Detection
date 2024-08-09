# Melanoma Detection
> Build a multiclass classification model using a custom convolutional neural network in TensorFlow. 


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. 
- What is the business probem that your project is trying to solve?: A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.
- What is the dataset that is being used?: The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- With the first model using rescale our accuracy was low and there was a huge gap between training and validation accuracy
- Introducing augmentation reduced the gap
- Rectifying class imbalance increased accuracy
- Final accuracy was still low as more training and accuracy was required.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
argcomplete==3.1.1
certifi==2024.2.2
charset-normalizer==3.3.2
click==8.1.7
colorama==0.4.6
idna==3.7
jsonpickle==3.0.2
packaging==23.1
pipx==1.2.0
requests==2.31.0
tqdm==4.66.4
urllib3==2.2.1
userpath==1.9.0
pandas==2.0.3
numpy==1.24.3
matplotlib==3.7.2
python==3.10.12
sklearn==1.3.0
keras==3.4.1
tensorflow==2.17.0
augmentor==0.2.12
<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->


## Contact
Created by [@chetnapriyadarshini] - feel free to contact me!