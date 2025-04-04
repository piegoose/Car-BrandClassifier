# Car Brand Classifier

This project demonstrates a deep learning model that classifies car brands based on input images. It uses transfer learning with a ResNet backbone and the fastai library to train an image classifier on a custom dataset of car images organized by brand.

## Overview

The model takes an image of a car and predicts its brand, such as BMW, Audi, or Mercedes. The dataset is organized into subfolders where each folder corresponds to a car brand.

## Features

- Image classification using convolutional neural networks (CNN)
- Transfer learning with pretrained ResNet18
- Two training strategies:
  - `fine_tune()` method (recommended for most use cases)
  - Manual freezing and unfreezing of layers using `fit_one_cycle()`
- Evaluation of model accuracy and training loss
- Interactive prediction interface using `ipywidgets`
- Easy-to-use notebook with clear structure and explanations

## Technologies

- Python
- fastai
- PyTorch
- Google Colab
- Jupyter Notebook

## Dataset

The dataset contains images of cars grouped into directories by brand. If the dataset is large, it is recommended to store it in Google Drive or download it using a script. Example datasets can be found on:

[Kaggle - Car Images by Brand](https://www.kaggle.com/datasets/elaroussi/car-images)

You may also include a small subset of sample images in a folder like `examples/` or `data/sample_images/` for demonstration purposes.


car-brand-classifier/
├── car_brand_classifier.ipynb   # Main training and testing notebook
├── car_classifier.py            # Python script version (optional)
├── data/                        # Example images or small subsets
├── export.pkl                   # Trained model
├── requirements.txt             # Dependencies (optional)
└── README.md


## Getting Started

1. Clone this repository or open the notebook in Google Colab:
   [Open in Colab](https://colab.research.google.com/github/your-username/car-brand-classifier/blob/main/car_brand_classifier.ipynb)

2. Mount your Google Drive and set the path to your dataset:
   ```python
   from google.colab import drive
   drive.mount('/content/gdrive')

