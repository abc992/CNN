# Melanoma Detection Assignment
> To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce much manual effort needed in diagnosis.

## Table of Contents
* Data Summary
* Project Pipeline
* Results


### Data Summary:

The dataset consists of 2,357 malignant and benign oncological diseases formed from the International Skin Imaging Collaboration (ISIC).   The images were stored in directories with the same name as the disease.

All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:
1. Actinic keratosis
2. Basal cell carcinoma
3. Dermatofibroma
4. Melanoma
5. Nevus
6. Pigmented benign keratosis
7. Seborrheic keratosis
8. Squamous cell carcinoma
9. Vascular lesion

### Project Pipeline
* Data Reading/Data Understanding → Defining the path for train and test images.
* Dataset Creation → Create train & validation dataset from the train directory with a batch size of 32. Also, make sure to resize images to `180x180`.
* Dataset visualization → Create a code to visualize one instance of all the nine classes present in the dataset.
* Model Building & training:
  - Create a CNN model, which can accurately detect nine classes present in the dataset. While building the model, rescale images to normalize pixel values between (0, 1).
  - Choose an appropriate optimizer and loss function for model training.
  - Train the model for 20 epochs.
  - Write our findings after the model fit. You must check if there is any evidence of model overfit or underfit.
* Choose an appropriate data augmentation strategy to resolve underfitting/overfitting
* Model Building & training on the augmented data:
  - Create a CNN model, which can accurately detect nine classes present in the dataset. While building the model, rescale images to normalize pixel values between (0, 1).
  - Choose an appropriate optimizer and loss function for model training.
  - Train the model for 20 epochs.
  - Write our findings after the model fit, and see if the earlier issue is resolved or not?
* Class distribution: Examine the current class distribution in the training dataset
  - Which class has the least number of samples? 
    Answer: seborrheic keratosis.
  - Which classes dominate the data regarding the proportionate number of samples? 
    Answer: pigmented benign keratosis.
  - melanoma and pigmented benign keratosis have a proportionate number of classes.
* Handling class imbalances: Rectify class imbalances in the training dataset with the Augmentor library.
* Model Building & training on the rectified class imbalance data:
  - Create a CNN model, which can accurately detect nine classes present in the dataset. While building the model, rescale images to normalize pixel values between (0, 1).
  - Choose an appropriate optimizer and loss function for model training.
  - Train the model for 50 epochs.
  - Write our findings after the model fit, and see if the issues are resolved or not?

### Results
- Results from 1st Model Building & Training: The model is overfitting because we can also see differences in loss functions in training & validation around the 6-8th epoch.
- Results after Model Building & Training on the Augmented Data: The Model accuracy is similar, but it is evident that the overfitting issue has been resolved due to data augmentation.
- Results after Model Building & Training on the Rectified Class Imbalance Data: Using the Augmentor library has improved the accuracy of the training data.

** Author
Nadeem Akhter


