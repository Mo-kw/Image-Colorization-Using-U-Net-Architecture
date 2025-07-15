# Image-Colorization-Using-U-Net-Architecture
This project implements a U-Net model in PyTorch to automatically colorize grayscale landscape images. It trains on paired grayscale and color images by predicting the chrominance channels from luminance inputs in Lab color space. Mixed precision training is used for faster GPU performance, and results are visualized by converting back to RGB.
