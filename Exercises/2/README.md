# Exploring the Impact of Inception Modules on CNN Accuracy

## Overview

In this assignment, the focus is on evaluating the impact of adding Inception Modules to a Convolutional Neural Network (CNN) model trained on the CIFAR-10 dataset. The task requires testing the model without any Inception Modules and then progressively adding one, two, and three Inception Modules to observe the changes in performance, particularly with regard to accuracy and overfitting.

## Project Structure

The project includes the following components:

- **main.ipynb**: The primary Jupyter notebook that implements the model variations and reports the results.
- **results/**: A directory containing images that visualize the outcomes of different experiments.
  - `Without_InceptionModule.png`: Results of the model without any Inception Modules.
  - `With_One_InceptionModule.png`: Results after adding one Inception Module.
  - `With_Two_InceptionModule.png`: Results after adding two Inception Modules.
  - `With_Three_InceptionModule.png`: Results after adding three Inception Modules.

## Experimentation and Results

### 1. Without Inception Module

The base model was implemented without any Inception Modules. The architecture includes three convolutional layers followed by a dense layer for classification. This model serves as the benchmark for evaluating the impact of the Inception Modules.

**Model Summary:**
- **Accuracy:** 64.52%
- **Overfitting:** The model suffers from overfitting, as indicated by a significant gap between the training and validation accuracy after the initial epochs.

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/2/results/Without_InceptionModule.png)

### 2. With One Inception Module

In the first variation, one Inception Module was added to the CNN model. This module is designed to improve the model’s ability to capture different features by applying convolution operations with different kernel sizes in parallel.

**Model Summary:**
- **Accuracy:** 68.87%
- **Overfitting:** Overfitting remains an issue, but there is a noticeable improvement in the validation accuracy compared to the baseline.

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/2/results/With_One_InceptionModule.png)

### 3. With Two Inception Modules

In the second variation, two Inception Modules were added to the model. The goal was to further enhance feature extraction and see if stacking Inception Modules could reduce overfitting.

**Model Summary:**
- **Accuracy:** 71.40%
- **Overfitting:** While overfitting still persists, the accuracy improvement suggests that the model benefits from the additional Inception Module.

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/2/results/With_Two_InceptionModule.png)

### 4. With Three Inception Modules

In the final variation, three Inception Modules were incorporated into the model. This setup aimed to maximize the depth and complexity of feature extraction while monitoring the impact on accuracy and overfitting.

**Model Summary:**
- **Accuracy:** 72.99%
- **Overfitting:** The accuracy further improves, but overfitting continues to be a challenge, with the validation accuracy plateauing after a few epochs.

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/2/results/With_Three_InceptionModule.png)

## Conclusion

Adding Inception Modules to the CNN model progressively increased the accuracy on the CIFAR-10 dataset, demonstrating the effectiveness of these modules in enhancing feature extraction. However, the issue of overfitting remained significant across all variations. While the Inception Modules improved the validation accuracy, the training accuracy consistently outpaced it, suggesting that further techniques, such as regularization, may be necessary to mitigate overfitting.

This assignment illustrates the trade-offs between model complexity and generalization in deep learning and highlights the importance of carefully tuning network architecture to achieve optimal performance.
