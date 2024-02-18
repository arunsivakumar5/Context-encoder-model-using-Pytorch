# Context-encoder-model-using-Pytorch
In this project, We created models to inpaint joints in knee radiography by using Context encoders which helps us remove surgical artifacts from knee radiograph images.

# Key Features:

## Introduction:
This GitHub repository presents a medical image artifact removal system powered by Context encoders. The primary objective of this project is to help users remove medical artifacts present in the images such as knee prostheses, screws, plates, or wires.

## Data Loading and Preprocessing:
The code starts by loading and preprocessing knee radiograph images. It performs various preprocessing steps, including separating artifact images within the dataset for regeneration using the trained model, handling negative images, and checking for blurry images.

## Generator and Discriminator Architectures: 
The code defines the architectures of the generator and discriminator neural networks. The generator takes in a image without context (without center part) as input and produces the center part as output. The generator is responsible for generating the context of the images (center of the image). The generator achieves this tasks by using the latent representations generated in the bottleneck of the architecture for each input image. The discriminator distinguishes between real and generated context. 

## Training Loop: 
The training loop iteratively trains the generator and discriminator networks. It uses adversarial training, where the generator tries to produce realistic context images to fool the discriminator, while the discriminator aims to distinguish between real and fake context images.

## Loss Functions: 
The code uses different loss functions, including binary cross-entropy loss (BCELoss) and mean squared error loss (MSELoss), to calculate the losses for both the generator and discriminator.

## Optimizers:
Adam optimizers are used to update the weights of the generator and discriminator networks during training.

## Monitoring and Saving: 
During training, the code monitors and saves various metrics, including discriminator and generator losses, FID scores (Fréchet Inception Distance), and sample images to visualize the training progress. FID is used to quantify the difference between real and generated fake images. 

# Conclusion
The generated fakes show that the generator part of our model is able to recreate the joint portion of knee radiographs. Thus we can utilize this encoder model to convert images with surgical artifacts into images without artifacts and re-introduce them into training/testing sets.
