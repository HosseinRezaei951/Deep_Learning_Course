# Deep Learning Course

Welcome to the Deep Learning Course repository. This collection of materials includes a series of exercises and a final project focused on various deep learning techniques and applications. The course covers Convolutional Neural Networks (CNNs), Inception Modules, VGG16 model modifications, and Autoencoders. Additionally, it features a project on generating music using Generative Adversarial Networks (GANs). Each section is designed to provide hands-on experience with Python scripts and Jupyter notebooks, facilitating practical learning and application of deep learning concepts.

## Directory Structure

### Exercises

The `Exercises` directory is divided into subdirectories, each focusing on different deep learning tasks and experiments:

#### Exercise 1: Improving CNN Model Accuracy on CIFAR-10 Dataset

This exercise involves enhancing a CNN model's accuracy on the CIFAR-10 dataset by adjusting hyperparameters and network architecture:

- **Results Directory**:
  - Contains images comparing the original model with modifications, including learning rate adjustments, dropout layers, and architectural changes.
  - Files: `original.png`, `learningRate.png`, `Dropout.png`, `changingLayers.png`.

- **Scripts**:
  - **main.ipynb**: Jupyter notebook implementing the original model and modifications, including results analysis.

#### Exercise 2: Exploring the Impact of Inception Modules on CNN Accuracy

This exercise evaluates the impact of adding Inception Modules to a CNN model trained on the CIFAR-10 dataset:

- **Results Directory**:
  - Includes images showing the performance of the model with different numbers of Inception Modules.
  - Files: `Without_InceptionModule.png`, `With_One_InceptionModule.png`, `With_Two_InceptionModule.png`, `With_Three_InceptionModule.png`.

- **Scripts**:
  - **main.ipynb**: Jupyter notebook implementing the model variations and reporting results.

#### Exercise 3: Evaluating VGG16 Performance with Modified Top Layers

This exercise explores how modifying the top layers of the VGG16 model affects its performance on the CIFAR-10 dataset:

- **Results Directory**:
  - Contains images comparing the performance of VGG16 with default and modified top layers.
  - Files: `Original.png`, `include_top.png`.

- **Scripts**:
  - **main.ipynb**: Jupyter notebook that tests VGG16 with various configurations and visualizes the results.

#### Exercise 4: Evaluating Variations in Autoencoder Performance

This exercise evaluates an autoencoder's performance with different configurations, including optimizer changes, epoch adjustments, and regularization:

- **Results Directory**:
  - Includes images comparing the autoencoder's performance with different settings.
  - Files: `Original.png`, `adam_optimizer.png`, `100_epochs.png`, `with_regularizationTerm.png`.

- **Scripts**:
  - **main.ipynb**: Jupyter notebook with code for autoencoder experiments and result analysis.

### Project: Music Generation Using GANs

The final project involves generating music using a GAN model trained on MIDI files. This project explores the use of GANs for creative applications:

- **Data Directory**:
  - Contains MIDI files used for training and data processing.
  - Files: `csp.npy`, `data.npy`, `GAN_generator.h5`, `newSong.mid`.

- **Input Directory**:
  - Contains MIDI files for training the GAN model.
  - Files: Various `.mid` files.

- **Scripts**:
  - **GAN_MusicGeneration.ipynb**: Jupyter notebook for implementing and training the GAN model, including music generation.

## How to Use

### Running the Jupyter Notebooks and Scripts

1. **Exercise 1 (CNN Accuracy Improvement)**:
   - Navigate to the `1` subdirectory under `Exercises` and open `main.ipynb` to experiment with model adjustments and view results.

2. **Exercise 2 (Inception Modules Impact)**:
   - Navigate to the `2` subdirectory under `Exercises` and open `main.ipynb` to analyze the effect of Inception Modules on model performance.

3. **Exercise 3 (VGG16 Modification)**:
   - Navigate to the `3` subdirectory under `Exercises` and open `main.ipynb` to explore VGG16 model variations and compare results.

4. **Exercise 4 (Autoencoder Variations)**:
   - Navigate to the `4` subdirectory under `Exercises` and open `main.ipynb` to evaluate the impact of different settings on autoencoder performance.

5. **Final Project (Music Generation with GANs)**:
   - Open `GAN_MusicGeneration.ipynb` in the `Project` directory using Google Colab or Jupyter Notebook. Follow the steps for data processing, model training, and music generation.

## Conclusion

This course provides a comprehensive introduction to various deep learning techniques and applications. Through practical exercises and a final project, you will gain hands-on experience and a deeper understanding of deep learning concepts. Explore the provided scripts and notebooks to enhance your learning and apply these techniques to your own projects.