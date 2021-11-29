# CSC490 Project - Melanoma Semantic Segmentation - Melanoma Boys

## Contributors
Alees Ahmad Goraya<br />
Xiaoyang Wu<br />
Brandon Elefano<br />
Harshraj Gohil<br />

## Introduction

Melanoma is one of the deadliest forms of cancer [1]. In 2021 alone, it is projected that 106,110 people will be diagnosed with the disease, and another 7,180 people will die because of it [2]. More and more people have been contracting this form of cancer within the past few decades, and it doesn’t seem like this trend will slow down anytime soon [2]. It is more common in older people, but its occurrence in young people (under 40) is not uncommon, and has been increasing in past years [3]. This demonstrates how Melanoma is a problem that affects a good part of our global population, regardless of age.

Early identification of cancer gives doctors more time to treat the disease, thus  increasing the chances that the patient will recover from it. However, many places lack the personnel to make those early diagnoses, as there has been a shortage of dermatologists in the past five years [1]. Cleverly designed neural networks could help make up for this lack of personnel, and potentially save numerous lives.

## Dataset

**Name:** ISIC 2017 Lesion Segmentation Challenge #1

**Size:** ~12GB total 

**Image Formats:** JPEG/PNG

**Challenge/Objective:** The dataset has dermoscopic images of skin lesions, the task is to automate predictions of skin lesion segmentation boundaries.

**Link:** https://challenge.isic-archive.com/landing/2017/42

## How to run

This notebook must be run on Google Colaboratory.

In order to run this, you need to have a folder titled CSC490 in your root directory. That folder must also contain folders titled:

*   Model (From this repository)
*   ISIC-2017_Training_Data
*   ISIC-2017_Training_Part1_GroundTruth 
*   ISIC-2017_Validation_Data
*   ISIC-2017_Validation_Part1_GroundTruth
*   ISIC-2017_Test_v2_Data
*   ISIC-2017_Test_v2_Part1_GroundTruth

The ISIC folders can be found here: [ISIC 2017 Challenge](https://challenge.isic-archive.com/data/#2017).

Moreover, you need to run the following from the repository root to compile the UNet weights:

    cd /Model/weight_unet
    cat weight_unet.?? > weights_unet.h5
    mv weights_unet.h5 ..
    
    cd ../weight_unet_preprocessed
    cat weight_unet_preprocessed.?? > weights_unet_preprocessed.h5
    mv weights_unet_preprocessed.h5 ..
    
You can also access the notebook [here](https://colab.research.google.com/drive/1rjuYMO7enxPjLzdPeYLmMtyXiDyHq3vH?usp=sharing).

## Sources
[1] N. C. Codella, D. Gutman, M. E. Celebi, B. Helba, M. A. Marchetti, S. W. Dusza, A. Kalloo, K. Liopyris, N. Mishra, H. Kittler, and A. Halpern, “Skin lesion analysis toward melanoma detection: A challenge at the 2017 International Symposium on Biomedical Imaging (ISBI), hosted by the International Skin Imaging Collaboration (ISIC),” 2018 IEEE 15th International Symposium on Biomedical Imaging (ISBI 2018), Jan. 2018.

[2] “Melanoma skin cancer statistics,” American Cancer Society. [Online]. Available:https://www.cancer.org/cancer/melanoma-skin-cancer/about/key-statistics.html. [Accessed: 02-Oct-2021].

[3] “Melanoma,” Mayo Clinic, 10-Mar-2020. [Online]. Available: https://www.mayoclinic.org/diseases-conditions/melanoma/symptoms-causes/syc-20374884. [Accessed: 02-Oct-2021].
