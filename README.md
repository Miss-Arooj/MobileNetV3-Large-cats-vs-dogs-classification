# Cats vs Dogs Image Classification

A transfer-learning image classification project using MobileNetV3-Large to distinguish cats from dogs. The notebook covers dataset loading, preprocessing, augmentation, training, validation, test evaluation, confusion matrices, and saving model weights.

## Highlights

- MobileNetV3-Large transfer learning.
- Image preprocessing and augmentation.
- Training, validation, and test evaluation.
- Validation and test confusion matrix visualizations.
- Model checkpoint export.

## Technology Stack

Python, PyTorch, Torchvision, MobileNetV3-Large, Scikit-learn, Matplotlib

## Dataset

The cat and dog images used in this project were self-collected. The dataset is not included in this repository. You must provide your own local copy using the directory structure expected by the notebook before running the training cells.

Expected dataset layout:

```text
dataset.zip
├── cats/
│   └── images/
├── dogs/
│   └── images/
└── test/
```

Keep the dataset locally; do not commit dataset archives or image files to this repository.

## Repository Contents

- `notebooks/cats-vs-dogs-classification.ipynb` — notebook for data preparation, model training, and evaluation.
- `outputs/validation_confusion_matrix.png` — validation set confusion matrix.
- `outputs/test_confusion_matrix.png` — test set confusion matrix.
- `requirements.txt` — Python dependencies.
- `.gitignore` — excludes local environments, datasets, and model artifacts.

## Setup

1. Clone this repository.
2. Create and activate a virtual environment.
3. Install the dependencies.

```bash
python -m venv .venv

# Windows PowerShell
.venv\Scripts\Activate.ps1

# macOS / Linux
source .venv/bin/activate

pip install -r requirements.txt
```

## Run / Reproduce

1. Place your self-collected dataset archive in the notebook's expected working directory as `dataset.zip`.
2. Open `notebooks/cats-vs-dogs-classification.ipynb` in Jupyter or Google Colab.
3. Update dataset paths if your archive uses a different folder structure.
4. Run the notebook cells in order. The notebook saves the trained model checkpoint locally.

The dataset, pretrained weights, and generated model checkpoint are not included in this repository.

## Results

Recorded notebook outputs:

- **Validation Accuracy:** 90.00%
- **Test Accuracy:** 95.00%

### Validation Confusion Matrix

![Validation Confusion Matrix](outputs/validation_confusion_matrix.png)

### Test Confusion Matrix

![Test Confusion Matrix](outputs/test_confusion_matrix.png)

These results are based on the recorded notebook outputs and should be reproduced with the same dataset split before being used in external claims.

## Limitations and Future Improvements

- The dataset is self-collected and is not distributed with this repository.
- Results depend on the collected images, dataset split, and training environment.
- Further evaluation on a larger and more diverse dataset could help assess generalization.
- Future improvements could include additional augmentation, hyperparameter tuning, and testing on unseen real-world images.