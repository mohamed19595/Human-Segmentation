# Human-Background Segmentation

This project focuses on human-background segmentation using deep learning techniques, specifically leveraging the U-Net architecture. The notebook includes data preprocessing, custom dataset creation, model training, and background replacement using the trained model.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dataset](#dataset)
- [Training](#training)
- [Background Replacement Filter](#background-replacement-filter)
- [Results](#results)
- [Acknowledgments](#acknowledgments)

## Features
- **Custom Dataset Class** with data augmentation capabilities.
- **Dice Loss** implementation for semantic segmentation.
- **U-Net Architecture** for segmentation.
- **Training Loop** with evaluation and visualization.
- **Background Replacement Filter** to replace the segmented background with custom images.

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Ensure you have access to a GPU if available (CUDA is recommended for training).

## Usage

1. **Prepare the Dataset**:
   - Organize your dataset in the required directory structure.
   - Update paths in the notebook accordingly.

2. **Run the Notebook**:
   - Open `playground.ipynb` and execute cells step-by-step.

3. **Training the Model**:
   - Modify hyperparameters as needed and run the training loop.

4. **Background Replacement**:
   - Use the provided filter to replace the background of input images.

## Project Structure
- **`playground.ipynb`**: The main notebook containing all the steps for preprocessing, model training, and testing.
- **`Models/`**: Directory to save trained model weights.
- **`Dataset/`**: Directory containing training and test datasets.
- **`requirements.txt`**: List of dependencies.

## Dataset
The dataset consists of images and corresponding masks for human segmentation. Ensure the following directory structure:
```
Dataset/
    |- Images/
    |- Masks/
```
- The images and masks should be aligned.
- Data augmentation is applied during training.

## Training
The training loop uses the following hyperparameters (modifiable in the notebook):
- Learning Rate: `0.0001`
- Epochs: `50`
- Batch Size: `4`
- Model Architecture: U-Net with `32` filters in the base layer.

## Background Replacement Filter
The trained model can replace the background of input images. Use the provided function in the notebook to:
1. Segment the image.
2. Replace the background with a custom image.

## Results
- The model achieves segmentation of human figures with high accuracy.
- Example outputs are visualized in the notebook.

## Acknowledgments
- This project uses PyTorch and torchvision for deep learning.
- Special thanks to the open-source community for pre-trained models and utilities.

