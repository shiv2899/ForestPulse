# ForestPulse - Deforestation Detection from Satellite Images

Detect forest loss from satellite images using U-Net segmentation + multi-date change detection.

> Built a deforestation monitoring pipeline using Sentinel-2 imagery, U-Net segmentation and multi-date change detection, visualized on an interactive map.

## Results
- Dataset: 5108 aerial images (256x256) - DeepGlobe / Forest Segmentation
- Model: U-Net with ResNet34 encoder
- Val IoU: 0.7713
- Train / Val Split: 80% / 20%

## What it does
1. Takes a satellite image -> predicts Forest Mask (White = Forest)
2. Compares Forest Mask 2020 vs 2024
3. Calculates Deforested Area in % + pixels
4. Visualizes loss in RED

## Demo
Forest 2020 vs Forest 2024 vs Deforested (RED = 15.3% loss)

## How to Run
1. Open `01_deforestation_setup_and_data.ipynb` in Google Colab
2. Enable T4 GPU: Runtime > Change runtime type > T4 GPU
3. Run all cells in order
4. Best model saves to `models/best_unet.pth`

## Tech Stack
Python, U-Net, ResNet34, Google Colab, Kaggle
