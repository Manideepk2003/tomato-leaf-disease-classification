# Tomato Leaf Disease Classification using CNN

## Project Overview

This project presents a deep learning based image classification system designed to detect diseases in tomato plant leaves. The system analyzes images of tomato leaves and automatically classifies them into multiple disease categories using Convolutional Neural Networks (CNN).

The objective of the project is to study the effectiveness of different CNN architectures for plant disease classification and analyze how architectural complexity affects classification performance. Multiple models are implemented and compared to evaluate their accuracy and computational efficiency.

Early detection of plant diseases is important in agriculture because it helps farmers take preventive actions before the disease spreads, thereby improving crop yield and reducing losses.

---

## Dataset

The dataset used in this project is the **Tomato Leaf Disease Dataset**, available publicly on Kaggle.

This dataset contains images of tomato leaves belonging to different disease categories as well as healthy leaves. The images are captured under different environmental conditions to ensure variability and robustness in model training.

### Dataset Details

* Total Classes: 10
* Training Images: ~10,000
* Validation Images: ~1,000
* Image Type: RGB leaf images

### Preprocessing Steps

Before training the models, the following preprocessing steps were applied:

* Image resizing to **224 × 224 pixels**
* Image normalization
* Dataset loading using PyTorch image loaders
* Separation of training and validation datasets

These preprocessing steps ensure compatibility with standard CNN architectures such as VGG16.

---

## Models Implemented

Three CNN architectures were implemented and evaluated in this project.

### 1. AlexNet

AlexNet is one of the earliest deep convolutional neural network architectures used for image classification.

* Implemented using **MATLAB Deep Learning Toolbox**
* Used as the baseline model for comparison
* Designed with multiple convolutional and fully connected layers

**Validation Accuracy:** ~70%

---

### 2. VGG16

VGG16 is a deeper CNN architecture known for its strong performance in image classification tasks.

* Implemented using **PyTorch**
* Transfer learning applied using pretrained **ImageNet weights**
* Training performed using **Google Colab (Tesla T4 GPU)**

The pretrained model allows faster convergence and improved accuracy by leveraging knowledge learned from large datasets.

**Validation Accuracy:** ~97.10%

---

### 3. Modified VGG16

A modified version of the VGG16 architecture was designed to analyze the effect of model complexity on performance.

Modification performed:

* One convolutional layer removed from the architecture

Objective of modification:

* Reduce computational complexity
* Observe impact on classification accuracy

**Validation Accuracy:** ~96.7%

The modified architecture achieved slightly lower accuracy while reducing model complexity, demonstrating the trade-off between performance and computational cost.

---

## Model Performance Comparison

| Model          | Validation Accuracy |
| -------------- | ------------------- |
| AlexNet        | 70%                 |
| VGG16          | 97.10%              |
| Modified VGG16 | 96.7%               |

From the results, it is clear that deeper CNN architectures such as **VGG16** significantly outperform simpler models like **AlexNet** for plant disease classification.

---

## Technologies Used

The following technologies and tools were used in this project:

* **Python** – Programming language for deep learning implementation
* **PyTorch** – Deep learning framework used for model training
* **MATLAB** – Used for AlexNet implementation
* **Google Colab** – Cloud-based GPU environment for training
* **Deep Learning (CNN)** – Core machine learning methodology
* **Computer Vision** – Image analysis and classification

---

## Project Workflow

The overall workflow of the project is summarized below:

1. Load and preprocess the dataset
2. Resize and normalize tomato leaf images
3. Load pretrained CNN architectures
4. Modify final classification layers
5. Train the models using GPU acceleration
6. Evaluate model performance using validation data
7. Compare CNN architectures based on accuracy and complexity

---

## How to Run the Project

### 1. Clone the repository

```
git clone https://github.com/Manideepk2003/tomato-leaf-disease-classification.git
```

### 2. Download the dataset

Download the **Tomato Leaf Disease Dataset** from Kaggle.

### 3. Extract the dataset

Place the dataset inside the project directory:

```
dataset/
```

### 4. Open the notebook

```
tomato_disease_cnn.ipynb
```

### 5. Run the notebook

The notebook can be executed using:

* **Google Colab**
* **Jupyter Notebook**

---

## Results

The experimental results demonstrate that transfer learning with pretrained CNN architectures significantly improves classification accuracy in plant disease detection tasks.

The VGG16 architecture achieved the highest accuracy, while the modified VGG16 model maintained competitive performance with slightly reduced computational complexity.

These findings highlight the importance of architecture selection when designing deep learning models for agricultural applications.

---

## Future Improvements

Several improvements can be explored in future work:

* Deploy the trained model as a **web application**
* Integrate the model with **IoT-based crop monitoring systems**
* Expand the dataset to include **more plant species**
* Implement **real-time disease detection using mobile devices**
* Apply advanced architectures such as **ResNet or EfficientNet**

---

## Author

**Manideep Kumar**
B.E Electronics and Communication Engineering
Sathyabama Institute of Science and Technology
