# Improving CNN Model Accuracy on CIFAR-10 Dataset

## Overview

This assignment focuses on improving the accuracy of a Convolutional Neural Network (CNN) model applied to the CIFAR-10 dataset. The task involves making modifications to an initial CNN model to address overfitting and enhance its performance. The adjustments include changing the learning rate, adding dropout layers, and altering the network architecture.

## Project Structure

The project includes the following key components:

- **main.ipynb**: The primary Jupyter notebook containing the original model implementation, subsequent modifications, and the resulting analysis.
- **results/**: A directory containing images that visualize the outcomes of different experiments conducted in the notebook.
  - `original.png`: Results of the model with no modifications.
  - `learningRate.png`: Results after adjusting the learning rate.
  - `Dropout.png`: Results after adding dropout layers.
  - `changingLayers.png`: Results after significant modifications to the network architecture.

## Improvement Techniques and Results

### Original Model

The original CNN model was trained on the CIFAR-10 dataset using a relatively simple architecture with multiple convolutional layers, followed by a fully connected layer. The model achieved high training accuracy but suffered from significant overfitting, with a validation accuracy of **68.44%**.

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/1/results/original.png)

### Learning Rate Adjustment

To address the overfitting issue, the learning rate of the optimizer (SGD) was reduced from `0.01` to `0.001`. This change aimed to slow down the training process and potentially yield better generalization. However, while this modification resulted in a slightly more stable training process, it did not significantly improve the validation accuracy.

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/1/results/learningRate.png)

### Adding Dropout Layers

In the next experiment, dropout layers with a rate of `0.2` were added after each convolutional layer to prevent overfitting by randomly dropping a fraction of the neurons during training. This adjustment significantly improved the model's performance on the validation set, reducing the validation loss and providing a more balanced accuracy between training and validation data.

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/1/results/Dropout.png)

### Architectural Changes

Further modifications were made by experimenting with different network architectures. This included adding more layers, changing the number of filters, and incorporating additional max-pooling and dropout layers. The model architecture was also switched from a functional to a sequential approach. These comprehensive changes effectively addressed the overfitting problem and significantly improved both training and validation accuracies.

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/1/results/changingLayers.png)

## How to Use

### Running the Jupyter Notebook

1. **Setup**:
   - Ensure you have the required libraries installed, such as `keras`, `matplotlib`, and `tensorflow`.
   - The notebook is designed to run on Google Colab with GPU acceleration for optimal performance.

2. **Original Model**:
   - Run the notebook sections corresponding to the original model to observe the initial results and overfitting issues.

3. **Apply Modifications**:
   - Sequentially run the cells that implement the learning rate adjustment, dropout layers, and architectural changes.
   - Observe the changes in the loss and accuracy plots after each modification.

4. **Visualize Results**:
   - Refer to the images in the `results/` directory for a visual comparison of the model's performance before and after each modification.

## Conclusion

This assignment demonstrates the importance of model tuning and architecture design in deep learning. By making systematic changes to the learning rate, adding regularization techniques such as dropout, and experimenting with different architectures, the overfitting issue was mitigated, and the model's generalization to unseen data was significantly improved. 

The results from this assignment can serve as a foundation for further exploration and optimization of CNN models for image classification tasks.
