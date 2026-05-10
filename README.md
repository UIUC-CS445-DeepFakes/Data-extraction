# Data-extraction

## Intro

This repository contains the code for extracting the datasets from Google Drive. The original datasets were downloaded from Kaggle then uplaoded(zipped) to Google Drive.
There are three datasets in total; namely, CelebDF, UADFV, Human Faces Dataset.
The CelebDF used in this projects is version 2. It contains 50.7k real and 50.7k fake images "split into ∼80% training, ∼10% validation, and ∼10% for testing."
UADFV contains a collection of 1.5k real and 1.5k fake images generated from the University at Albany DeepFake Video.
Human Faces contains approximatly 9.6k human faces. Around 5k human faces and 4.6k AI generated faces.

## Our Dataset

We used 22,702 images from across datasets. To maintain a balanced dataset, we choose all the images from the Human Faces and UADFV, while randomly selecting 10,000 images from the CelebDFV2 dataset. The datasets were divided using an approximate 70% training, 15% testing, and 15% validation. Several preprocessing techniques were used to extract and divide the data before training: 
* Split-folders library to split the Human Faces dataset.
* Random Samples from predefined train, test and Val folders with classification labels for CelebDFV2 dataset.
* GroupShuffleSplit to group data by videos when splitting UADFV
The images labels included their datasets’ name and class label to avoid conflict when merging the datasets. After preprocessing, each dataset was compressed and stored in Google Drive. 

| DataSet | Training | Validation |   Test  |  Total  | 
|---------|---------|-------------|---------| --------|
|CelebDFV2| 3,500 Real & 3,500 Fake| 750 Real & 750 Fake| 750 Real & 750 Fake| 10,000 |
|UADFV| 1,068 Real & 1,044 Fake| 224 Real & 224 Fake  | 256 Real & 256 Fake   |3,072 |
|Human Faces| 3,500 Real & 3,241 Fake| 750 Real & 694 Fake|750 Real & 695 Fake| 9,630|


## Dataset Sources
- CelebDFV2: https://www.kaggle.com/datasets/pranabr0y/celebdf-v2image-dataset 
- UADFV: https://www.kaggle.com/datasets/adityakeshri9234/uadfv-dataset 
- Human Faces: https://www.kaggle.com/datasets/kaustubhdhote/human-faces-dataset

## Coding Sources
- How to Generate a Train-Test-Split Based on a Group ID? https://www.geeksforgeeks.org/machine-learning/how-to-generate-a-train-test-split-based-on-a-group-id/
- SplitFolder: https://pypi.org/project/split-folders/
- Zip file extraction: https://medium.com/@i.doganos/extracting-and-renaming-files-from-zip-archives-in-python-3c015ec21280

## Devloper
- Aleem Prince: aleemap2@illinois.edu

## To run this code:
1. Open this notebook in Google Colab.
2. Create a Shortcut for the Datasets(link) in your Drive: https://drive.google.com/drive/folders/1xUYj5THC66V4iy6QEUNEvhkGRm3tPcqP?usp=sharing
   * CELEBDF.zip
   * HUMAN FACES.zip
   * UADFV.zip
3. Run the program.
   
## Libraries
- ```from google.colab import drive```
- ```import random```
- ```import os```
- ```import zipfile as zip```
- ```import cv2```
- ```import matplotlib.pyplot as plt```
- ```from sklearn.model_selection import GroupShuffleSplit```
- ```import shutil```
- ```import re```
- ```import splitfolders``` Might need ```!pip install split-folders```

