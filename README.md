# Human-Background Segmentation

This project focuses on human-background segmentation using deep learning techniques, specifically leveraging the U-Net architecture. The notebook includes data preprocessing, custom dataset creation, model training, and background replacement using the trained model.


## Features
- **Custom Dataset Class** with data augmentation capabilities.
- **Dice Loss** implementation for semantic segmentation.
- **U-Net Architecture** for segmentation.
- **Training Loop** with evaluation and visualization.
- **Background Replacement Filter** to replace the segmented background with custom images.

## Project Structure
- **`playground.ipynb`**: The main notebook containing all the steps for preprocessing, model training, and testing.


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
- The model achieves segmentation of human figures.
- Example outputs are visualized in the notebook.


