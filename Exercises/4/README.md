# Evaluating Variations in Autoencoder Performance

## Overview

In this assignment, we evaluate the impact of different modifications on the performance of an autoencoder model trained on the MNIST dataset. Specifically, we experiment with changing the optimizer, adjusting the number of epochs, and adding regularization to the encoder. The goal is to understand how these changes affect the model's reconstruction performance and image quality.

## Project Structure

The project includes the following components:

- **main.ipynb**: The primary Jupyter notebook that contains the code for the autoencoder experiments and results.
- **results/**: A directory containing images that visualize the outcomes of different experiments.
  - `Original.png`: Results of the original autoencoder model.
  - `adam_optimizer.png`: Results after changing the optimizer to 'adam'.
  - `100_epochs.png`: Results after increasing the number of epochs to 100.
  - `with_regularizationTerm.png`: Results after adding L1 regularization to the encoder.

## Experimentation and Results

### 1. Original Autoencoder

The base model, as originally provided, uses the 'adadelta' optimizer with 50 epochs and no regularization. The model architecture includes a simple encoder and decoder, and it serves as the benchmark for evaluating the impact of further modifications.

**Model Summary:**
- **Initial Loss:** Approximately 0.7210
- **Final Loss (Epoch 50):** Approximately 0.4410
- **Image Quality:** The reconstructed images are noticeably less clear and exhibit significant artifacts, particularly in thinner parts of the digits.

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/4/results/Original.png)

### 2. Autoencoder with Adam Optimizer

In this variation, the optimizer was changed from 'adadelta' to 'adam'. The model was trained with the same number of epochs (50). The 'adam' optimizer generally provides better convergence and faster training.

**Model Summary:**
- **Initial Loss:** Approximately 0.3846
- **Final Loss (Epoch 50):** Approximately 0.0926
- **Image Quality:** The reconstructed images show a substantial improvement in quality compared to the original model. The reconstructions are closer to the original images with reduced artifacts.

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/4/results/adam_optimizer.png)

### 3. Autoencoder with 100 Epochs

For this experiment, the number of epochs was increased from 50 to 100 while keeping the 'adam' optimizer. This change aims to give the model more training time to refine its performance.

**Model Summary:**
- **Initial Loss:** Approximately 0.3809
- **Final Loss (Epoch 100):** Approximately 0.0923
- **Image Quality:** The reconstructed images are very similar to those from the 50-epoch run with 'adam', with potentially minor improvements in detail. There is some additional noise in darker areas of the images.

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/4/results/100_epochs.png)

### 4. Autoencoder with Regularization Term

In this variation, L1 regularization was added to the encoder layer with a regularization term of \(10^{-5}\). The objective is to assess how regularization impacts model performance and reconstruction quality.

**Model Summary:**
- **Initial Loss:** Approximately 0.3929
- **Final Loss (Epoch 50):** Approximately 0.0988
- **Image Quality:** The reconstructed images are similar in quality to those obtained with the 'adam' optimizer and 50 epochs, but there is a slight increase in noise, especially in the darker regions of the images. Regularization has slightly impacted the smoothness of the reconstructions.

![alt text](https://github.com/HosseinRezaei951/Deep_Learning_Course/blob/main/Exercises/4/results/with_regularizationTerm.png)

## Conclusion

Each modification provided valuable insights into the performance of the autoencoder:

- **Optimizer Change:** Switching to 'adam' significantly improved the loss and quality of image reconstructions.
- **Increasing Epochs:** Extending the training period to 100 epochs yielded marginal improvements in reconstruction quality but did not drastically change the results compared to 50 epochs with 'adam'.
- **Adding Regularization:** Incorporating L1 regularization slightly impacted reconstruction quality, particularly introducing more noise in darker regions.

These experiments demonstrate the importance of optimizing hyperparameters and regularization techniques to enhance model performance and image reconstruction quality.