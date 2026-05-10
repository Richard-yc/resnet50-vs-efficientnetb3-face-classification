# Data

The dataset files are not included directly in this repository because of file size.

## Primary Dataset

This project uses a real-vs-fake face image dataset for binary image classification.

Dataset name: Kaggle 140k Real and Fake Faces  
Dataset link: [https://www.kaggle.com/datasets/xhlulu/140k-real-and-fake-faces]

Please download the dataset manually from the source above.

The reproducibility notebooks currently assume the dataset is located on the Desktop. I recommend renaming the dowonload folder to:
```text
real-vs-fake
```
If you store the dataset somewhere else, update the dataset path variable near the top of the notebooks.

## Primary Dataset Expected Folder Structure

After downloading, extracting, and renaming the folder, the folder structure should look like this:

```text
Desktop/
└── real-vs-fake/
    ├── test.csv
    ├── train.csv
    ├── valid.csv
    └── real_vs_fake/
        └── real-vs-fake/
            ├── train/
            │   ├── real/
            │   └── fake/
            ├── valid/
            │   ├── real/
            │   └── fake/
            └── test/
                ├── real/
                └── fake/
```

The image folder used by the notebook is:

```text
Desktop/real-vs-fake/real_vs_fake/real-vs-fake/
```

## Additional dataset
These datasets were used for unseen-data evaluation.

Unseen Dataset A

Dataset name: Kaggle 130k Real and Fake Faces  
Dataset link: [https://www.kaggle.com/datasets/shreyanshpatel1/130k-real-vs-fake-face]

Unseen Dataset B

Dataset name: HuggingFace Deepfake vs real  
Dataset link: [https://huggingface.co/datasets/prithivMLmods/Deepfake-vs-Real/tree/main]

Note: You may need a Hugging Face account to download this dataset.
