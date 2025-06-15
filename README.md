# UNet for Histopathology Cell Segmentation

This project uses a UNet model to perform cell segmentation on histopathology patches, with the goal of testing how well synthetically generated patches support downstream segmentation tasks.

We work with Lizard-v2 data and predict segmentation masks and 6 types of nuclei annotations:
- epithelial
- lymphocyte
- plasma
- eosinophil
- neutrophil
- connective tissue.

# File Overview

- main.py: Runs segmentation on patches, computes Dice scores, and saves predicted masks.
- prepare_patches.ipynb: Prepares training data from the raw Lizard-v2 format.

# Expected folder structure:

  ```sh
../data/lizard_v2/
├── images/train/
├── classes/train/
└── instances/train/
  ```

# Usage

1. Run prepare_patches.ipynb to create patches.
2. Then run main.py to perform segmentation and evaluate results.
