# Evaluating VGG16 Performance with Modified Top Layers

## Overview

In this assignment, we explore the impact of modifying the VGG16 model architecture, specifically by adjusting the `include_top` parameter. The goal is to understand how these changes affect the model's performance on the CIFAR-10 dataset. Initially, we use VGG16 with its default settings and then modify it by setting `include_top` to `False`, adding new classification layers, and comparing the results.

## Project Structure

The project consists of the following components:

- **main.ipynb**: The primary Jupyter notebook that implements and tests the VGG16 model with various configurations.
- **results/**: A directory containing images that visualize the results of the experiments.
  - `Original.png`: Results of the VGG16 model with the default `include_top=True`.
  - `include_top.png`: Results of the VGG16 model with `include_top=False` and additional classification layers.

## Experimentation and Results

### 1. VGG16 with Default Configuration

In this configuration, VGG16 is used with its default settings, including the fully connected layers (`include_top=True`). This setup uses the pre-trained weights of VGG16 and is designed to classify the CIFAR-10 dataset directly.

**Model Summary:**
- **Train Loss:** 0.15997
- **Test Loss:** 1.47129
- **Train F1 Score:** 0.96864
- **Test F1 Score:** 0.71210

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/3/results/Original.png)

### 2. VGG16 with Modified Top Layers

In the second experiment, the `include_top` parameter of VGG16 is set to `False`, removing the original classification layers. New classification layers are added on top of the VGG16 base. This modification aims to observe if altering the final layers affects the model's performance.

**Model Summary:**
- **Train Loss:** 0.15993
- **Test Loss:** 1.30830
- **Train F1 Score:** 0.96428
- **Test F1 Score:** 0.70030

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/3/results/include_top.png)

## Analysis

### Default Configuration

With the original configuration (`include_top=True`), the model achieved high accuracy on the training set but showed a significant drop in test performance, indicating overfitting. The training loss decreased rapidly, while the validation loss plateaued after a certain number of epochs.

### Modified Configuration

When the top layers were removed and replaced with new classification layers (`include_top=False`), the model's test loss improved slightly, and the F1 Score decreased marginally. This suggests that while the new layers did not drastically improve the performance, there was a small positive effect on the test loss. The training and validation accuracy curves showed similar trends as in the default configuration, with a noticeable shift in the test loss.

## Conclusion

Modifying the VGG16 model by changing the `include_top` parameter and adding new classification layers resulted in minor improvements in test loss. However, the overall performance metrics did not show significant enhancement compared to the original model configuration. This suggests that while the additional classification layers can potentially fine-tune the model, they may not always lead to substantial improvements in performance for every dataset.

This assignment highlights the impact of model architecture changes on performance and demonstrates that while adjusting final layers can be useful, careful consideration and experimentation are required to achieve optimal results.