# ResNet-50 vs EfficientNet-B3 Face Classification

This repository contains the code, notebooks, results, and dataset instructions for a comparative study of **ResNet-50** and **EfficientNet-B3** for real-vs-fake face image classification.

The goal of this project is to compare two convolutional neural network architectures on a binary image classification task and evaluate how well each model performs on both the original held-out test set and additional unseen datasets.

## 1. Project Overview

This project compares:

- **ResNet-50**
- **EfficientNet-B3**

Both models were trained and evaluated for binary classification:

```text
real face image vs fake face image
```
## 2. Repository Structure

```text
resnet50-vs-efficientnetb3-face-classification/
├── README.md
├── .gitignore
├── data/
│   └── README.md
├── notebooks/
│   ├── final/
│   │   ├── ResNet50_FINAL.ipynb
│   │   └── EfficientNetB3_FINAL.ipynb
│   ├── reproducibility/
│   │   ├── ResNet50_Reproducibility.ipynb
│   │   └── EfficientNet_B3_Reproducibility.ipynb
│   └── experiments/
│       ├── ResNet50_experiments.ipynb
│       └── EfficientNetB3_experiments.ipynb
└── results/
    ├── README.md
    ├── tables/
    └── plots/
```
## 3. Notebooks

The final notebooks provide the cleanest summary of the project and should be reviewed first.

'notebooks/final/ResNet50_FINAL.ipynb'
'notebooks/final/EfficientNetB3_FINAL.ipynb'

### Reproducibility Notebooks

The reproducibility notebooks are cleaner notebooks intended for rerunning evaluation or testing model configurations.
```text
notebooks/reproducibility/ResNet50_Reproducibility.ipynb
notebooks/reproducibility/EfficientNet_B3_Reproducibility.ipynb
```
### Experiment Notebooks

The experiment notebooks contain the original model development process, including baseline runs, tuning attempts, intermediate comparisons, and final model selection.
```text
notebooks/experiments/ResNet50_experiments.ipynb
notebooks/experiments/EfficientNetB3_experiments.ipynb
```

## 4. Dataset
The dataset files are not included directly in this repository because of file size.

Primary dataset:

Kaggle 140k Real and Fake Faces
Dataset link: https://www.kaggle.com/datasets/xhlulu/140k-real-and-fake-faces

Additional unseen evaluation datasets:

Kaggle 130k Real and Fake Faces
https://www.kaggle.com/datasets/shreyanshpatel1/130k-real-vs-fake-face
Hugging Face Deepfake vs Real
https://huggingface.co/datasets/prithivMLmods/Deepfake-vs-Real/tree/main

More detailed dataset setup instructions are available in:
```text
data/README.md
```
### Expected Dataset Structure
The reproducibility notebooks currently assume the main dataset is located on the Desktop and renamed to:

```text
real-vs-fake
```

## 5. Results

Saved result tables and plots are included in the `results/` folder

```text
results/
├── README.md
├── tables/
└── plots/
```

The `results/tables/` folder contains CSV summaries of final configurations, tuning summaries, and evaluation metrics.

The `results/plots/` folder contains final visual summaries, including confusion matrices, final metric plots, and model comparison plots.

## 6. Final Model Summary

### ResNet-50 
Final selected ResNet-50 run: __R13__

Final selected configuration:

+ Optimizer: AdamW
+ Learning rate: 1e-4
+ Weight decay: 1e-3
+ Augmentation: light
+ Batch size: 8
+ Scheduler: ReduceLROnPlateau

### EfficientNet-B3

Final selected EfficientNet-B3 run: __E07__

Final selected configuration:

+ Optimizer: AdamW
+ Learning rate: 3e-4
+ Weight decay: 1e-3
+ Augmentation: light
+ Batch size: 8
+ Scheduler: none

## 7. How to Run
1. Clone this repository:
```text
git clone https://github.com/Richard-yc/resnet50-vs-efficientnetb3-face-classification.git
cd resnet50-vs-efficientnetb3-face-classification
```
2. Install the required Python libraries.
Recommended libraries include:

```text
torch
torchvision
numpy
pandas
matplotlib
scikit-learn
Pillow
tqdm
jupyter
```
3. Download the datasets listed in the Dataset Section
4. Follow the dataset setup instructions in 'data/REAME.md'
5. Open the notebooks in Jupyter Notebook, JupyterLab, VS Code, or Google Colab
   
Recommended review order:
1. notebooks/final/
2. notebooks/reproducibility/
3. notebooks/experiments/

### 8. Notes on Reproducibility

The final notebooks summarize completed results and do not retrain the models.

The reproducibility notebooks are intended for rerunning evaluation or testing configurations.

The experiment notebooks contain the original tuning process and may show paths or outputs from the local runtime environment used during development.

## 9.  Contributors (ECE 4990)
Richard Yam Ciau, Ulyses Ortega, Tran Vo

ECE 4990- Department of Electrical and Conputer Engineering
Fall 2026
