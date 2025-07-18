# PlantLDNet-Disease-Detection-in-Leaf-Images-Using-Deep-Learning-Models

PlantLDNet is a purpose-built convolutional neural network (CNN) tailored for the task of plant leaf disease detection and classification. This custom architecture enables precise identification of multiple plant diseases through image analysis, focusing on robust performance across diverse agricultural conditions.

## Table of Contents
- [Project Overview](#project-overview)
- [Models Used](#models-used)
- [Dataset](#dataset)
- [Results](#results)
- [Contributors](#contributors)

## Project Overview
The PlantLDNet model leverages a custom CNN architecture comprising six 2D convolutional layers, four max-pooling layers, and ReLU activation functions. The architecture harnesses batch normalization and selective feature loss at key stages, promoting the extraction of refined and discriminative features, leading to improved leaf disease classification performance. Attention is given to stable training and robust generalization.

### 1. Cluster Layer One (CL_1)
-Initial Convolution
-**5×5 kernel**
-**128 feature maps**
-Hierarchical Convolution
-**Two successive 5×5 convolutions with 128 filters each**
-Pooling and Dimensionality Reduction
-**Three max-pooling layers, each with a 3×3 kernel, to progressively reduce spatial dimensions**
-Batch Normalization & Dropout
-**30% dropout encourages sparsity and robustness, decorrelates learned weights**
-Output
-**Feature map size reduced to 13×13×64**

### 2. Cluster Layer Two (CL_2)
-Convolutional Pair
-**Two convolutional layers, each with 64 filters of size 5×5**
-Pooling
-**Two consecutive max-pooling layers, 2×2 each, reduce features to 3×3×64**

### 3. Cluster Layer Three (CL_3)
-Final Convolution
-**Single convolutional layer with 32 filters of 3×3 kernel size**
-Pooling
-**Max-pooling (2×2) reduces output to 1×1×32**

### 4. Fully Connected (Feed-Forward) Layers
-First Dense Layer
-**128 neurons, ReLU activation**
-Output Layer
-**3 neurons, Softmax activation**


## Dataset

The dataset used for this project is a combination of publicly available MRI brain tumor datasets. It includes:
- **Healthy**: 1000 images
- **Early Blight**: 1000 images
- **Late Blight**: 1000 images

Images are resized to 150x150 pixels, pre-processed, and normalized for training.

## Results

The ensemble model achieved the following performance metrics:
- **Accuracy**: 99.95%
- **Precision**: 96%
- **Recall**: 96%
- **F1-Score**: 96%

The **ROC curve** demonstrates perfect classification with an AUC of 1.0 for all four classes.

## Contributors

- Gurram Sai Nikhileswar
- Kodela Chaithanya krishna
- Surya Sai Pampana
- Chintalapudi Likhitha Bhavana
- Rayanki Lakshmi Nanditha
