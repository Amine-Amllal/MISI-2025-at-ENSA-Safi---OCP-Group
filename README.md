# Computer Vision: Detection of Seaming Defects on Sardine Cans

This project was built for **Hackaton Safi 2025** and focuses on detecting visual defects in sardine can seaming using a YOLOv8 object detection pipeline.

## Achievement

We won **1st place** in this competition.

## Project Goal

Build an automated computer vision workflow that can identify seaming defects from images, helping quality control processes become faster and more consistent.

## Repository Contents

- `training (1).ipynb`: Main notebook used for training, evaluation, and inference.

## Training Workflow (from the notebook)

The notebook follows this sequence:

1. Check GPU availability in Colab.
2. Install dependencies:
   - `ultralytics`
   - `roboflow`
3. Download dataset from Roboflow in YOLOv8 format.
4. Train YOLOv8 (`yolov8n.pt` base model) with:
   - image size: `640`
   - epochs: `50`
   - batch size: `16`
5. Validate model performance (`model.val()`).
6. Visualize training/evaluation outputs:
   - confusion matrix
   - precision/recall and confidence curves
   - prediction samples
7. Load best weights and run test predictions on random or uploaded images.

## Typical Environment

This workflow is designed for **Google Colab** (GPU recommended), then exporting artifacts (`.zip`) for local use.

## Main Dependencies

- Python 3.x
- Ultralytics YOLOv8
- Roboflow
- PyTorch
- PIL / IPython display utilities

## Notes

- The notebook currently contains a Roboflow API key in plain text. It is strongly recommended to move it to an environment variable or secret manager before sharing publicly.
- Large datasets and binary assets are intentionally excluded from version control via `.gitignore`.

## Team

I participated in this competition with the following teammates:

- ZOUGA Mouhcine
- FARIS Amine
- EL MADANI Adam
