# Exploring and Analyzing ControlNet for Image Generation

## Overview
This project explores the accuracy of image generation using ControlNet, a model introduced to add conditions to text-to-image diffusion models. The focus is on the Canny edge detection model within ControlNet and analyzing image generation based on Canny images from a dataset.

## Dependencies
Make sure to install the required dependencies:

```bash
!pip install -q diffusers==0.14.0 transformers xformers git+https://github.com/huggingface/accelerate.git
!pip install -q opencv-contrib-python
!pip install -q controlnet_aux
!pip install torchmetrics
```

## Dataset Preparation
1. **Dataset Structure:**
   - Place your original horse dataset in the directory `/content/drive/MyDrive/input_horses`.
   - Place your original horse dataset in the directory `input_horses`.

2. **Canny Image Generation:**
   - The script converts the horse dataset to Canny images for analysis.
@@ -31,7 +31,7 @@ Make sure to install the required dependencies:
## Image Generation
1. **Generating Images:**
   - Images are generated based on the Canny images using the ControlNet pipeline.
   - Generated images are stored in `/content/drive/MyDrive/generated_horses_org` and `/content/drive/MyDrive/generated_horses_res`.
   - Generated images will get stored in `generated_horses_org` and `generated_horses_res`.

## Accuracy Measurement using LPIPS
1. **LPIPS Calculation:**
   - Learned Perceptual Image Patch Similarity (LPIPS) is used to measure the accuracy of generated images.
   - LPIPS scores are calculated and visualized for both original and resized images.
2. **Mean LPIPS:**
   - The mean LPIPS scores are calculated for both org and resized images.
## Conclusion
This project provides insights into the accuracy of image generation using ControlNet's Canny edge detection model. Further analysis and experimentation can be conducted to enhance the understanding of the model's performance.
