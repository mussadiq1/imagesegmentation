# Technical Assessment Submission by Dr. Mussadiq Abdul Rahim  

## Overview  
This repository contains a segmentation model implementing a semi-supervised student-teacher approach, utilizing pretrained model weights and partial cross-entropy loss. The dataset used is "(Resized) aerial-imagery-for-roof-segmentation," available on Kaggle, courtesy of [atilol](https://www.kaggle.com/atilol).  

## Dataset  
The dataset should be placed in Google Drive in the following directories:  
- `TRAIN_PATH = '/content/drive/MyDrive/AIRS/train'`  
- `VAL_PATH = '/content/drive/MyDrive/AIRS/val'`  
- `TEST_PATH = '/content/drive/MyDrive/AIRS/test'`  

If running locally, update these paths as needed. The dataset is referred to as **AIRS** throughout the project.  

## Prerequisites  
Ensure all required packages are installed before running the notebook. This includes necessary libraries for data loading, model training, and visualization.  

## Notebook Structure  
1. **Necessary Imports and Google Drive Mounting** – Import required libraries and mount Google Drive for dataset access.  
2. **Configurations** – Set up configurations for training, including model parameters and paths.  
3. **Dataset Loading** – Load the dataset from the specified directories.  
4. **Segmentation Classes** – Define the segmentation classes used in model training.  
5. **TheDataset Class** – Custom class to load images from dataset paths.  
6. **Helper Function for Data Visualization** – Functions to visualize images and segmentation masks.  
7. **Load and Visualize TheDataset Class** – Display samples from the dataset.  
8. **Semi-Supervised Learning** –  
    - **student_model** is initialized using the pretrained model **BACKBONE**.  
    - **teacher_model** is initialized as a copy of the student model.  
9. **Experiments** – Uncomment specific configurations to run different experiments.  
10. **Train Step and Update Teacher Weights Functions** – Functions for model training and updating teacher weights.  
11. **Model Training** – Training the student model while updating the teacher model.  

## Acknowledgment  
This project uses parts of the data loading technique inspired by [atilol](https://www.kaggle.com/atilol) on Kaggle. Special thanks for making the "(Resized) aerial-imagery-for-roof-segmentation" dataset available.  

## Running the Notebook  
- **Google Colab**: Place the dataset in Google Drive as indicated above.  
- **Local Setup**: Update the paths accordingly to match your local file system.  

## Citation  
If using this implementation, kindly cite the original dataset source:  
```bibtex
@misc{atilol_roof_segmentation,
  author = {atilol},
  title = {(Resized) aerial-imagery-for-roof-segmentation},
  year = {2021},
  publisher = {Kaggle},
  howpublished = {\url{https://www.kaggle.com/atilol/aerial-imagery-for-roof-segmentation}}
}
