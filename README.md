# UNet for Histopathology Cell Segmentation

This project applies a UNet architecture for semantic segmentation of nuclei in histopathology patches. The core objective is to evaluate how well **synthetically generated** histology images support **downstream cell segmentation**, particularly in low-data or domain-shift scenarios.

We use the **Lizard-v2 dataset** and predict both **segmentation masks** and **nuclear subtype annotations**, spanning six clinically relevant cell types:
- Epithelial  
- Lymphocyte  
- Plasma  
- Eosinophil  
- Neutrophil  
- Connective Tissue

---

## File Overview

- `main.py` — Performs segmentation on prepared patches, computes **Dice scores**, and saves visualized prediction masks.
- `prepare_patches.ipynb` — Converts raw Lizard-v2 data into model-ready patches with matching labels.

---

## Expected folder structure
Make sure your data is organized like this:
  ```sh
../data/lizard_v2/
├── images/train/
├── classes/train/
└── instances/train/
  ```

---

## Usage

1. Run `prepare_patches.ipynb` to preprocess and patchify Lizard-v2 images.  
2. Then execute `main.py` to train the UNet model, perform segmentation, and evaluate performance (e.g., Dice coefficient).

---

## Results

We evaluate segmentation performance using per-class **Dice scores** and provide qualitative comparisons of predicted vs ground-truth masks for both real and synthetic samples.
