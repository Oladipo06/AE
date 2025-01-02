### Fashion MNIST Autoencoder
This repository contains a TensorFlow implementation of an autoencoder trained on the Fashion MNIST dataset. The autoencoder learns to compress fashion item images into a 2-dimensional latent space and reconstruct them back to their original form.
Overview
The project demonstrates:

Building and training an autoencoder using TensorFlow/Keras
Encoding fashion items into a 2D latent space
Reconstructing fashion items from their latent space representations
Generating new fashion items by sampling from the latent space

### Requirements

TensorFlow
NumPy
Matplotlib
Jupyter Notebook

### Dataset
The project uses the Fashion MNIST dataset, which consists of 70,000 grayscale images of clothing items across 10 categories. Each image is 28x28 pixels.
Model Architecture
The autoencoder consists of two main components:
### Encoder

Input shape: (32, 32, 1)
Three convolutional layers with increasing filters (32, 64, 128)
Flattening layer
Dense layer outputting 2-dimensional embeddings

### Decoder

Input shape: (2,)
Dense layer to reshape
Three transposed convolution layers (128, 64, 32)
Final convolution layer to reconstruct the image

### Usage

Clone the repository
```
https://github.com/Oladipo06/AE.git
```
Install the required dependencies
```
pip install -r requirements.txt
```
Open and run the Jupyter notebook autoencoder.ipynb

The notebook is structured in sections:

Data preparation
Model building
Training
Reconstruction demonstration
Latent space visualization
Image generation from the latent space

Model Training
The model is trained with:

Binary crossentropy loss
Adam optimizer
Batch size of 100
3 epochs by default

Training progress is monitored using TensorBoard and model checkpoints are saved automatically.
Results
The notebook demonstrates:

Reconstruction of test images
2D visualization of the latent space
Generation of new fashion items by sampling from the latent space
Color-coded visualization of different clothing categories in the latent space

Model Outputs
Models are saved in the following locations:

Complete autoencoder: ./models/autoencoder
Encoder: ./models/encoder
Decoder: ./models/decoder
