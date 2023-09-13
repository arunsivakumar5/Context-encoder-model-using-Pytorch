# Context-encoder-model-using-Pytorch
In this project, We created models to inpaint joints in knee radiography by using Context encoders which helps us remove surgical artifacts from knee radiograph imagesIn this project, We designed algorithms and models to inpaint joints in knee radiography by using Context encoders which helps us remove surgical artifacts from knee radiograph images

# Introduction:
This GitHub repository presents a medical image artifact removal system powered by Context encoders. The primary objective of this project is to help users remove medical artifacts present in the images such as knee prostheses, screws, plates, or wires.

## Data Loading and Preprocessing:
The code starts by loading and preprocessing knee radiograph images. It performs various preprocessing steps, including removing artifacts, handling negative images, and checking for blurry images.

## Generator and Discriminator Architectures: 
The code defines the architectures of the generator and discriminator neural networks. The generator is responsible for generating context images, while the discriminator distinguishes between real and generated context images.

## Training Loop: 
The training loop iteratively trains the generator and discriminator networks. It uses adversarial training, where the generator tries to produce realistic context images to fool the discriminator, while the discriminator aims to distinguish between real and fake context images.

## Loss Functions: 
The code uses different loss functions, including binary cross-entropy loss (BCELoss) and mean squared error loss (MSELoss), to calculate the losses for both the generator and discriminator.

## Optimizers:
Adam optimizers are used to update the weights of the generator and discriminator networks during training.

## Monitoring and Saving: 
During training, the code monitors and saves various metrics, including discriminator and generator losses, FID scores (Fréchet Inception Distance), and sample images to visualize the training progress.

