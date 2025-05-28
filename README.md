# Image-Inpainting

This project implements an **Image Inpainting Model** designed to fill in missing or corrupted regions in images. The model aims to intelligently predict and restore the content of the masked areas, producing visually coherent and contextually accurate reconstructions.

## Dataset
https://www.kaggle.com/datasets/theblackmamba31/landscape-image-colorization

##  Features

- **Edge Detection Guided Inpainting:** The model uses edge detection (Canny, Sobel, etc.) to guide the inpainting process.
- **GAN Architecture:** Combines a U-Net-based generator and a PatchGAN discriminator for realistic results.
- **Custom Training Logic:** Includes a custom training loop with validation and sample generation.
- **Preprocessing Pipelines:** Supports loading, resizing, masking, and edge detection of images.
- **Configurable Parameters:** Easily adjustable hyperparameters for experimentation.

##  Model Architecture

- **Generator:** U-Net with skip connections, multi-scale feature extraction, and edge guidance.
- **Discriminator:** PatchGAN discriminator to ensure local realism.
- **Loss Functions:** Combines adversarial loss, L1 loss, and edge consistency loss for effective training.

##  Dependencies

Install the following dependencies before running the code:

```bash
pip install tensorflow numpy matplotlib opencv-python scikit-image
