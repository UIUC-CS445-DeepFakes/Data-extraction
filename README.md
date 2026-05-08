# Data-extraction

## Intro

This repository contains the code for extracting the datasets from Google Drive. The original datasets were downloaded from Kaggle then uplaoded to Google Drive.
There are three datasets in total; namely, CelebDF, UADFV, Human Faces Dataset.
The CelebDF used in this projects is version 2. It contains 50.7k real and 50.7k fake images "split into ∼80% training, ∼10% validation, and ∼10% for testing."
UADFV contains a collection of 1.4k real and 1.5k fake images generated from the University at Albany DeepFake Video.
Human Faces contains approximatly 9.6k human faces. Around 5k human faces and 4.6k AI generated faces.

## Our Dataset

Using these datasets our data contains the following distribution:
| DataSet | Training | Validation |   Test  |  Total  | 
|---------|---------|-------------|---------| --------|
|CelebDFV2| 3.5k Real & Fake| 750 Real & Fake| 750 Real & Fake| 10k |
|UADFV| 1044 Real & 1044 Fake| Real & 1044 Fake  |Real & 1044 Fake   |Real & 1044 Fake  |
|Human Faces| 70%| 15%|15%| 100%|


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
