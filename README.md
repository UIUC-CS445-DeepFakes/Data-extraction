# Data-extraction

## Intro

This repository contains the code for extracting the datasets from Google Drive. The original datasets were downloaded from Kaggle then uplaoded to Google Drive.
There are three datasets in total; namely, CelebDF, UADFV, Human Faces Dataset.
The CelebDF used in this projects is version 2. It contains 50.7k real and 50.7k fake images "split into ∼80% training, ∼10% validation, and ∼10% for testing."
UADFV contains a collection of 1.5k real and 1.5k fake images generated from the University at Albany DeepFake Video.
Human Faces contains approximatly 9.6k human faces. Around 5k human faces and 4.6k AI generated faces.

## Our Dataset

Using these datasets our data contains 22,702 images with the following distribution:
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
- ```import splitfolders```

## Author
Aleem Prince: aleemap2@illinois.edu
