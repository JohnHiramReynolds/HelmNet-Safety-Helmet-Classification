# HelmNet — Safety Helmet Image Classification

**Computer Vision & Deep Learning Portfolio Project**  
**Author:** John Hiram Reynolds

## Project Overview

HelmNet is a computer vision project developed to classify construction workers as wearing or not wearing safety helmets using convolutional neural networks (CNNs).

The project explores deep learning architectures, transfer learning, and data augmentation to evaluate their effectiveness in binary image classification.

This is an image classification project, not a deployed real-time object detection system.

## Technologies Used

- Python
- TensorFlow / Keras
- OpenCV
- NumPy and pandas
- scikit-learn
- Matplotlib
- Jupyter Notebook / Google Colab

## Dataset

The project used **631 labeled images**:

- 311 images of workers wearing helmets
- 320 images of workers without helmets
- Image dimensions: 200 × 200 pixels, RGB

**Data preparation:**
- Stratified training, validation, and testing splits
- 441 training images
- 95 validation images
- 95 testing images
- Pixel normalization from 0–255 to 0–1

## Model Development

Four deep learning configurations were evaluated:

1. **Custom CNN:** Baseline convolutional neural network.
2. **VGG16:** Pretrained feature extraction using transfer learning.
3. **VGG16 + FFNN:** VGG16 with a feed-forward neural network classification head.
4. **VGG16 + FFNN + Data Augmentation:** Additional augmentation to support generalization.

Model performance was evaluated using confusion matrices and classification metrics.

## Recorded Results

The selected fourth model recorded the following results on the notebook's 95-image test set:

| Metric | Recorded Result |
|---|---|
| Accuracy | 100% |
| Weighted Precision | 100% |
| Weighted Recall | 100% |
| Weighted F1 Score | 100% |
| Correct Predictions | 95 of 95 |

The confusion matrix recorded 48 correctly classified no-helmet images and 47 correctly classified helmet images.

**Important:** These are results saved in the original notebook, not independently reproduced findings. The small test set and potential image duplication require further evaluation before making claims about real-world reliability.

## Reproducing the Experiment

1. Open `HelmNet_Completed.ipynb` in Jupyter Notebook or Google Colab.
2. Install the libraries listed in `requirements.txt`.
3. Obtain the original `Images.npy` and `Labels.csv` datasets from an authorized source.
4. Adjust the dataset paths in the notebook.
5. Run the notebook sequentially.

The original notebook did not pin dependency versions, so some compatibility adjustments may be necessary.

## Limitations and Future Improvements

The current implementation performs whole-image classification. It does not yet perform real-time object localization or multi-object tracking.

Areas for further development include:

- Auditing the dataset for duplicate and near-duplicate images.
- Evaluating performance on independent external datasets.
- Analyzing class-specific recall and false negatives.
- Exploring real-time video inference and object tracking.
- Investigating embedded AI deployment and inference latency.

## Repository Contents

- `HelmNet_Completed.ipynb` — Original experiment and recorded outputs, with a brief explanatory note.
- `requirements.txt` — Python dependencies.
- `README.md` — Project documentation.

## Project Context

This project was completed as part of my applied AI and machine learning education through The University of Texas at Austin.

My continuing professional interests include computer vision, real-time perception, embedded machine learning, robotics, and autonomous systems.

*Educational and research portfolio project. No claim of production deployment or certified safety performance.*
