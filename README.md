# Monkeypox-Skin-Lesion-Dataset

![License](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset/blob/main/Assests/cc.png)

The recent monkeypox outbreak has become a global healthcare concern owing to its rapid spread in more than 65 countries around the globe. To obstruct its expeditious pace, early diagnosis is a must. But the confirmatory Polymerase Chain Reaction (PCR) tests and other biochemical assays are not readily available in suffiecient quantities. In this scenario, computer-aided monkeypox identification from skin lesion images can be a beneficial measure. Nevertheless, so far, such datasets are not available. Hence, the ["Moneypox Skin Lesion Dataset (MSLD)"](https://www.kaggle.com/datasets/nafin59/monkeypox-skin-lesion-dataset) is created by collecting and processing images from different means of web-scrapping i.e., from news portals, websites and publicly accessible case reports. <br />

Some sample images from the dataset:<br />


![Sample Images](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset/blob/main/Assests/sample%20images.png)


This repository gives access to the Moneypox Skin Lesion Dataset. The creation of this dataset is primarily focused on distinguishing the monkeypox cases from the similar non-monkeypox cases. Therefore, along with the 'Monkeypox' class, we included skin lesion images of 'Chickenpox' and 'Measles' because of their resemblance to the monkeypox rash and pustules in initial state in another class named 'Others' to perform binary classification.<br />

The dataset itself is available for download at the [Kaggle](https://www.kaggle.com/datasets/nafin59/monkeypox-skin-lesion-dataset) or the [Google Drive](https://drive.google.com/drive/folders/1bIYqAW-vqDBq3Ou_UMXPwgemqfZeqQi5?usp=sharing).<br />

* * *

# Dataset Description

<!-- ![Data Division](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset/blob/main/Assests/data.JPG) -->

There are 3 folders in the dataset.<br />

1) Original Images: It contains a total number of ***228*** images, among which **102 belongs to the 'Monkeypox' class** and the remaining ***126 represents the 'Others' class i.e., non-monkeypox (chickenpox and measles) cases.***<br />

2) Augmented Images: To aid the classification task, several data augmentation methods such as rotation, translation, reflection, shear, hue, saturation, contrast and brightness jitter, noise, scaling etc. have been applied using MATLAB R2020a. ALthough this can be readily done using ImageGenerator, to ensure reproducibility of the results, the augmented images are provided in this folder. ***Post-augmentation, the number of images increased approximately 14-folds; the classes 'Monkeypox' and 'Others' have 1428 and 1764 images, respectively.***<br />

3) Fold1: To avoid any sort of bias in training, three-fold cross validation was performed. The original images were split into training, validation and test set(s) with the approximate proportion of 70 : 10 : 20 while maintaining patient independence. According to the commonly perceived data preparation practice, the training and validation images were augmented while the test set contained only the original images.<br />

![Data Preparation](https://github.com/ShamsNafisaAli/Monkeypox-Skin-Lesion-Dataset/blob/main/Assests/data_split.png)

* * *


# Sample Notebook for Classification

To see, how you can use this dataset for performing binary classification, please refer to the following notebooks:<br />
- [Notebook1](https://www.kaggle.com/code/gpiosenka/monkey-pox-f1-score-90) <br />
- [Notebook2](https://www.kaggle.com/code/nafin59/monkeypox-sample-classification-notebook)<br />

* * *


# Citation

If this dataset helped your research, please cite:<br />

Ali, S. N., Paul, J., Ahmed, M. T., Jahan, T., Sani,  S. M. Sakeef, Noor, N., & Hasan, T. (2022). Monkeypox Skin Lesion Detection Using Deep Learning Models: A Preliminary Feasibility Study. arXiv preprint arXiv:2xxx.xxxxx.

<blockquote>
  
@article{Nafisa2022,<br />
  title={Monkeypox Skin Lesion Detection Using Deep Learning Models: A Preliminary Feasibility Study},<br />
  author={Ali, Shams Nafisa and Paul, Joydip and Ahmed, Md. Tazuddin and Jahan, Tasnim and Sani,  Sani, S. M. Sakeef and Noor, Nawshaba and Hasan, Taufiq},<br />
  journal={arXiv preprint arXiv:2xxx.xxxxx},<br />
  year={2022}<br />
}

 
<!-- Tschandl, P., Rosendahl, C. & Kittler, H. The HAM10000 dataset, a large collection of multi-source dermatoscopic images of common pigmented skin lesions. Sci. Data 5, 180161 doi:10.1038/sdata.2018.161 (2018).  -->
