# 🌄 Landscape Image Colorization using U-Net and PyTorch

This project implements a deep learning-based solution for automatic image colorization using a U-Net architecture in PyTorch. It focuses on transforming grayscale landscape images into realistic colorized versions.

## 📌 Overview

Colorizing grayscale images is a classic problem in computer vision. In this project:

- A custom dataset of landscape images is used, split into grayscale and color versions.
- A U-Net model is trained to predict the chrominance (`ab`) components from the luminance (`L`) channel of Lab color space.
- The output is reconstructed into RGB images for visualization.
- Mixed Precision Training (AMP) is used for faster and more efficient training on GPU.

## 🧠 Model

The U-Net architecture is composed of:

- **Encoder**: Downsampling layers that capture context.
- **Decoder**: Upsampling layers with skip connections to restore resolution.
- Final output is a 2-channel tensor (`ab` channels), applied with `tanh` activation.

## 🏋️‍♂️ Training

- **Loss Function**: MSELoss between predicted and ground truth `ab` channels.
- **Optimizer**: Adam
- **Training Epochs**: 20
- **Batch Size**: 16
- **Validation Split**: 10% of dataset
- **AMP**: Mixed precision training with `torch.cuda.amp`

## 📊 Visualization

After training, a subset of the test dataset is visualized by displaying grayscale inputs alongside their colorized outputs.

![Sample Colorization Output](https://github.com/Mo-kw/Image-Colorization-Using-U-Net-Architecture/raw/main/sample.png)

## 💾 Model Saving and Loading

The trained model is saved as `colorization_unet.pth` and can be reloaded for inference.

## 🚀 Requirements

- Python 3.8+
- PyTorch
- OpenCV
- scikit-image
- matplotlib
- tqdm
- kagglehub

## 🔧 Usage

1. Install dependencies
2. Download dataset using `kagglehub`
3. Train the model with provided code
4. Visualize predictions

## 📓 Google Colab Notebook

The full implementation, including data loading, model definition, training loop, and visualization, is available in the [Google Colab Notebook here](https://colab.research.google.com/github/Mo-kw/Image-Colorization-Using-U-Net-Architecture/blob/main/Image_Colorization_Using_U_Net_Architecture.ipynb).



---

> 🔍 **Note**: Make sure to update file paths according to your local environment or Google Colab when running the notebook.

## 📜 License

This project is open source and available under the [MIT License](LICENSE).
