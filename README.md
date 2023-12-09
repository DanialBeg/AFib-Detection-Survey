# AFib-Detection-Survey
*Authors: Danial Beg and Sahithi Chimmula*

## Table of Contents
- [Overview](#overview)
- [Datasets](#datasets)
- [File Structure](#file-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)

## Overview
This project aims to detect atrial fibrilation (AFib) utilizing ECG waveform data provided in the PTB-XL dataset. A write-up of this project will be included soon but feel free to check our [final presentation](https://docs.google.com/presentation/d/11tC2UQEtE6XmAJ3CLjxVw6vJAPjzYQzvVvH-oDwDBV0/edit?usp=sharing)

## Datasets
Some of the datasets are too big to include on GitHub and thus can be downloaded from the following links: [ecgeq-500hzsrfava.npy](https://drive.google.com/file/d/1Ah1yqVCcW7cpN0mRJX9px1NWpYygi6CG/view?usp=share_link) and [af_dataset.csv](https://drive.google.com/file/d/1fErgzku6iusVsB5RxPjy4pKiCeOhbFFA/view?usp=share_link)

Once downloaded, please put them into the `data` folder to run the notebooks.

## File Structure
```
AFib-Detection-Survey/
│
├── src/ # Source files
│ ├── Inference Notebok.ipynb # Main script running inference through saved model files
│ └── LSTM_Training.ipynb # How the LSTM training was done
│ └── MLP_and_LogRegression.ipynb # How the MLP and Logistic Regression training was done
│ └── Final_Transformer.ipynb # How the Transformer training was done (unweighted)
│ └── Final_Transformer_weighted.ipynb # How the Transformer training was done (weighted)
│
├── data/ # Data files
│ └── coorteeqsrafva.csv # Patient demographic CSV
│ └── ecgeq-500hzsrfava.npy # ECG waveform data for all patients  NOTE: PLEASE DOWNLOAD FROM GOOGLE DRIVE
│ └── af_dataset.csv # Combined ECG waveform and patient demographic data NOTE: PLEASE DOWNLOAD FROM GOOGLE DRIVE
│
├── saved_models/ # Saved Models
│ └── simple_mlp_model.pth # MLP saved model
│ └── lstm_saved.h5 # LSTM saved model
│ └── logistic_regression_model.pkl # Logistic Regression saved model
│
└── README.md # Project documentation
```
