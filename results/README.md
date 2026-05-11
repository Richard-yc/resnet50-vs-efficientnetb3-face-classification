# Results

This folder contains saved result tables and plots from the final model evaluation.

The full model summaries are shown in the final notebooks:

- `notebooks/final/ResNet50_FINAL.ipynb`
- `notebooks/final/EfficientNetB3_FINAL.ipynb`

## Tables

The `tables/` folder contains CSV files summarizing final configurations, tuning summaries, and evaluation metrics.

Included files:

```text
results/tables/
├── resnet50_best_config.csv
├── resnet50_tuning_summary.csv
├── resnet50_final_metrics.csv
├── efficientnetb3_best_config.csv
├── efficientnetb3_tuning_summary.csv
├── efficientnetb3_final_metrics.csv
└── model_comparison.csv
```

## Plots

The `plots/` folder contains visual summaries of the final model results.

Included files:

```text
results/plots/
├── resnet50_test_confusion_matrix.png
├── resnet50_unseen_a_confusion_matrix.png
├── resnet50_unseen_b_confusion_matrix.png
├── efficientnetb3_test_confusion_matrix.png
├── efficientnetb3_unseen_a_confusion_matrix.png
├── efficientnetb3_unseen_b_confusion_matrix.png
├── resnet50_tuning_val_f1.png
├── resnet50_final_metrics_by_dataset.png
├── resnet50_loss_by_dataset.png
├── efficientnetb3_tuning_val_f1.png
├── efficientnetb3_final_metrics_by_dataset.png
├── efficientnetb3_loss_by_dataset.png
├── model_comparison_f1_by_dataset.png
└── model_comparison_accuracy_by_dataset.png
```

## Notes

This folder is intended for final summary results only.

Intermediate tuning runs, training histories, and exploratory outputs are kept in the experiment notebooks:

`notebooks/experiments/ResNet50_experiments.ipynb`

`notebooks/experiments/EfficientNetB3_experiments.ipynb`
