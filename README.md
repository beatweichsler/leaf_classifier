# Leaf_Classification_DL: Classifying Leaf Species Using Deep Learning

## Project Overview

This notebook is a personal project aimed at exploring deep learning methods, inspired by the Deep Learning course at DTU (02456). The project was uploaded to the [Kaggle Leaf Classification Challenge](https://www.kaggle.com/competitions/leaf-classification/overview), where it achieved a score of 0.192. The goal was to classify various leaf species using image data along with three other feature sets: margin, shape, and texture.

## Repository Contents

- **Jupyter Notebook**: Code for loading, preprocessing, training, and evaluating the model.
- **Dataset Files**:
  - `train.csv`: Training data for the model.
  - `test.csv`: Testing data for model evaluation.
  - `sample_submission.csv`: A sample file in the required submission format.
  - `images/`: Folder containing the leaf image files, each named with a unique ID.

## Dataset Description

The dataset was provided by James Cope, Thibaut Beghin, Paolo Remagnino, and Sarah Barman from the Royal Botanic Gardens, Kew, UK. For further details, refer to the publication: 

> Mallah, C., Cope, J., & Orwell, J. (2013). *Plant Leaf Classification Using Probabilistic Integration of Shape, Texture and Margin Features.* Signal Processing, Pattern Recognition and Applications, in press.

### Data Fields

- **id**: Unique identifier for each image.
- **margin_1, margin_2, ..., margin_64**: Attribute vectors for the margin feature.
- **shape_1, shape_2, ..., shape_64**: Attribute vectors for the shape feature.
- **texture_1, texture_2, ..., texture_64**: Attribute vectors for the texture feature.

The dataset consists of images of leaf samples along with 64-dimensional vectors for each feature (margin, shape, and texture), which collectively aid in classification.

## Methodology

### Model Architecture

The model architecture integrates multiple deep learning techniques:
- **Convolutional Neural Networks (CNNs)**: To extract spatial features from images.
- **Recurrent Neural Networks (RNNs)**: To analyze sequential shape data, leveraging its temporal dependencies.
- **Feed-Forward Neural Networks (FFNNs)**: For margin and texture data processing.
  
These methods are combined in a custom architecture to capture diverse feature information effectively.

### Training Process

Training is performed using the cross-entropy loss function, which is suitable for multi-class classification. The model is trained with high dropout and batch normalization to prevent overfitting, and evaluations are logged for training and validation accuracy.

### Code Reuse

Some code snippets and utilities were reused from the DTU Deep Learning course (02456).

## Getting Started

### Setting Up

1. **Clone or Download the Repository**: Clone this repository or download it as a ZIP file.
2. **Data Preparation**: Ensure that `train.csv`, `test.csv`, `sample_submission.csv`, and the `images/` folder are in the same directory as the notebook.

### Running the Notebook

1. **Open Jupyter Notebook**: Launch the notebook in a Jupyter environment.
2. **Execute Cells Sequentially**: Run the cells in order to replicate the analysis and train the model.
