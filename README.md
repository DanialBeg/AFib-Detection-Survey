# AFib-Detection-Survey
*Authors: Danial Beg (dbeg@uci.edu) and Sahithi Chimmula (schimmul@uci.edu)*

## Table of Contents
- [Overview](#overview)
- [Datasets](#datasets)
- [File Structure](#file-structure)
- [Installation](#installation)
- [Usage](#usage)
  
## Overview
This project aims to detect atrial fibrilation (AFib) utilizing ECG waveform data provided in the PTB-XL dataset. A write-up of this project can be found [here](https://www.overleaf.com/read/drkdsxcwmwhk#ff5a8e) and please feel free to check out our [final presentation](https://docs.google.com/presentation/d/11tC2UQEtE6XmAJ3CLjxVw6vJAPjzYQzvVvH-oDwDBV0/edit?usp=sharing)

## Datasets
Some of the datasets are too big to include on GitHub and thus can be downloaded from the following links: [ecgeq-500hzsrfava.npy](https://drive.google.com/file/d/1Ah1yqVCcW7cpN0mRJX9px1NWpYygi6CG/view?usp=share_link) and [af_dataset.csv](https://drive.google.com/file/d/1fErgzku6iusVsB5RxPjy4pKiCeOhbFFA/view?usp=share_link).

Once downloaded, please put them into the `data` folder to run the notebooks.

Additionally, please download [output_file.pt](https://drive.google.com/file/d/1O67MLnU0iU9AZoaDHG3z_AIH-pPyVQi3/view?usp=sharing) from Google Drive and place it under `src/transformer_data/`.

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
│ └── Pre_processing_Transformer.ipynb # How the data passed into the transformer was pre-processed, generated output stored in /transformer_data/
└── transformer_data/                # Model training notebooks
│       ├── labels.pt               # Labels tensor
│       ├── other_features_file.pt  # Patient demographic tensor
│       └── output_file.pt          # Pre-processed ECG tensor              NOTE: PLEASE DOWNLOAD FROM GOOGLE DRIVE
│
├── data/ # Data files
│ └── coorteeqsrafva.csv # Patient demographic CSV
│ └── ecgeq-500hzsrfava.npy # ECG waveform data for all patients            NOTE: PLEASE DOWNLOAD FROM GOOGLE DRIVE
│ └── af_dataset.csv # Combined ECG waveform and patient demographic data   NOTE: PLEASE DOWNLOAD FROM GOOGLE DRIVE
│
├── saved_models/ # Saved Models
│ └── simple_mlp_model.pth                  # MLP saved model
│ └── lstm_saved.h5                         # LSTM saved model
│ └── logistic_regression_model.pkl         # Logistic Regression saved model
│ └── transformer_model_unbalanced.pth      # Unweighted transformer saved model
│ └── transformer_model.pth                 # Weighted transformer saved model
│
└── README.md # Project documentation
```

## Usage
The main file to run is `Inference Notebok.ipynb` as it utilizes all the saved models and then runs inference with these models. Please ensure the file structure follows the convention as outlined in [File Structure](#file-structure).

The rest of the notebooks under `src` contain the code for the preprocessing and the training of the models that can be looked at as a reference.
