# OCR Character Recognition with CNN Architectures

This project provides a comparative analysis of several state-of-the-art Convolutional Neural Network (CNN) architectures, including DenseNet121, ResNet50, MobileNetV3Large, and EfficientNetB0, to determine their efficacy in classifying images of alphanumeric characters, specifically focusing on lowercase letters.

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Models Architecture](#models-architecture)
4. [Benefits of Specific Layers](#benefits-of-specific-layers)
5. [Callbacks for Model Training](#callbacks-for-model-training)
6. [Data Splitting](#data-splitting)
7. [Models Comparison](#models-comparison)
8. [Installation](#installation)
9. [Usage](#usage)
10. [Results](#results)
11. [License](#license)

## Introduction
This project aims to identify the most effective CNN architecture for classifying images of augmented characters. By leveraging a comprehensive dataset and implementing various data augmentations, the study evaluates the performance of different CNN models based on metrics like accuracy, precision, recall, and F1-score.

## Dataset
The dataset used is the OCR-Dataset, designed for Optical Character Recognition (OCR) tasks. It includes over 200,000 images of alphanumeric characters, generated using 3,475 different font styles. This project focuses specifically on lowercase characters (26 classes from 'a' to 'z'). Various data augmentation techniques, such as brightness adjustment and nearest neighbor filling, were applied to enhance the models' robustness.

## Models Architecture
The project explores different CNN architectures, each with its unique design philosophy:
- **DenseNet121**: Known for dense connectivity, promoting feature reuse.
- **ResNet50**: Incorporates residual connections, allowing for deeper networks.
- **MobileNetV3Large**: Optimized for mobile devices, reducing computational complexity.
- **EfficientNetB0**: Uses compound scaling for balanced network dimensions and efficiency.

## Benefits of Specific Layers
1. **DenseNet121**
   - **Dense Connectivity**: Enhances feature reuse and mitigates the vanishing gradient problem.
   - **Benefit**: Improved gradient flow and network efficiency.

2. **ResNet50**
   - **Residual Blocks**: Allows training of deeper networks without degradation.
   - **Benefit**: Enhanced performance in deeper architectures.

3. **MobileNetV3Large**
   - **Depth-wise Separable Convolutions**: Reduces parameters and computational cost.
   - **Benefit**: Suitable for mobile and edge devices with high performance.

4. **EfficientNetB0**
   - **Compound Scaling**: Balances network depth, width, and resolution.
   - **Benefit**: Achieves high performance with fewer parameters.

## Callbacks for Model Training
The project utilizes several callbacks to optimize training:
- **EarlyStopping**: Stops training if the validation performance stops improving.
- **ReduceLROnPlateau**: Reduces the learning rate when performance plateaus.
- **ModelCheckpoint**: Saves the model after every epoch for safety.

## Data Splitting
The dataset was split into training, validation, and testing sets:
- **Training and Testing Split**: 70% Training and 30% Testing.
- **Training and Validation Split**: The training set was further split into 75% Training and 25% Validation.

## Models Comparison
- **DenseNet121**: Achieved the highest performance with an accuracy of 0.96.
- **EfficientNetB0**: Comparable performance with fewer parameters.
- **MobileNetV3Large**: Strong performance, optimized for mobile and edge devices.
- **ResNet50**: Lower performance, possibly due to the specific characteristics of the dataset.

## Installation
To run this project locally, clone the repository and install the necessary dependencies:
```bash
git clone https://github.com/yourusername/ocr-character-recognition.git
cd ocr-character-recognition
pip install -r requirements.txt
```

## Usage
1. Prepare the dataset as described in the project.
2. Run the training script to train the models:
   ```bash
   python train.py
   ```
3. Evaluate the models using the evaluation script:
   ```bash
   python evaluate.py
   ```
4. Compare the results to determine the most effective model.

## Results
The project found that DenseNet121 outperforms other architectures in classifying the augmented character images, making it the most effective model for this specific task.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to contribute to this project by submitting issues or pull requests. Your feedback and improvements are always welcome!
