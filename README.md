# Breast-Cancer-Detection

## Purpose
The purpose of this project is to detect breast cancer from CT scans using image segmentation. I built two models in both PyTorch and Tensorflow using UNETs of different architectures.

        

## Methodology
One UNET was built in Tensorflow and Keras, the architecture contains 2 - 3x3 convolutional layers per block and uses 5 blocks on both the contracting and expanding path to get the image into a latent space with dimension 256. The model also used a batch size of 32 and trained for 10 epochs. Using BCE Dice loss the model achieved 0.9 validation accuracy. The other UNET was built in PyTorch, I experimented with many loss functions including dice, BCE dice, BCE, focal loss, and Tversky loss. I also tuned the model with hyperparameter grids to achieve higher accuracy. The optimized model ended up bringing the image to 1024 dimensions in latent space before the expanding path. The best loss function was binary cross entropy which resulted in roughly 0.4 dice loss during testing.
