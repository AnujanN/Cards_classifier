# 🃏 Card Image Classifier

A PyTorch-based deep learning project for classifying playing card images using transfer learning with ResNet18.

## 📋 Project Overview

This project implements a convolutional neural network to classify 53 different types of playing cards (52 standard cards + joker) using computer vision techniques.

### 🎯 Key Features
- **Transfer Learning**: Uses pre-trained ResNet18 model
- **Data Augmentation**: Comprehensive image transformations for better generalization
- **Interactive Training**: Jupyter notebook with progress visualization
- **High Accuracy**: Achieves 83%+ validation accuracy in just 3 epochs
- **Comprehensive Evaluation**: Includes prediction visualization and confidence scores

## 🏗️ Project Structure

```
card-classifier/
├── classifier.ipynb          # Main Jupyter notebook
├── requirements.txt          # Python dependencies
├── cards.csv                # Dataset metadata
├── .gitignore               # Git ignore rules
├── README.md                # Project documentation
├── train/                   # Training images (53 card classes)
├── valid/                   # Validation images
└── test/                    # Test images


## 📊 Dataset

The dataset contains **8,140 total images** distributed as:
- **Training**: 7,624 images
- **Validation**: 265 images  
- **Test**: 251 images

### Card Classes (53 total)
- 52 standard playing cards (Ace through King, 4 suits)
- 1 Joker class

## 🔬 Model Architecture

- **Base Model**: ResNet18 (pre-trained on ImageNet)
- **Transfer Learning**: Fine-tuned final layer for 53-class classification
- **Input Size**: 224×224×3 RGB images
- **Parameters**: ~11.2M total parameters

## 📈 Training Results

### Performance Metrics
- **Best Validation Accuracy**: 83.02%
- **Training Epochs**: 3 (initial run)
- **Optimizer**: Adam (lr=0.001, weight_decay=1e-4)
- **Loss Function**: CrossEntropyLoss

### Training Progress
| Epoch | Train Acc | Valid Acc | Train Loss | Valid Loss |
|-------|-----------|-----------|------------|------------|
| 1     | 35.77%    | 63.40%    | 2.35       | 1.18       |
| 2     | 67.03%    | 78.49%    | 1.18       | 0.76       |
| 3     | 74.40%    | 83.02%    | 0.90       | 0.58       |

## 🎮 Usage

### Training the Model
Run all cells in the `classifier.ipynb` notebook sequentially:

1. **Environment Setup**: Import libraries and check GPU availability
2. **Data Exploration**: Analyze dataset structure and visualize samples
3. **Data Pipeline**: Create DataLoaders with augmentation
4. **Model Creation**: Initialize ResNet18 with transfer learning
5. **Training Loop**: Train and validate the model
6. **Evaluation**: Visualize results and save the model

