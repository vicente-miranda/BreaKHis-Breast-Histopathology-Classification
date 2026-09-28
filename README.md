# BreaKHis breast histopathology classification

A Python workflow for classifying BreaKHis breast tissue images as benign or malignant, and by tumor subtype. It includes data preparation, exploratory analysis, and CNN and VGG16 training experiments.

## Data and setup

The images are not included. Set `source_directory` in `setup_data.py` to the folder containing `BreaKHis_v1 2/`, then install the requirements and prepare the splits:

```bash
pip install -r requirements.txt
python setup_data.py
```

This creates `data/train`, `data/val`, and `data/test` and updates `image_metadata/updated_image_data.csv`.

## Notebooks

`notebooks/eda.ipynb` explores the image metadata and class distribution. `notebooks/model_tuning.ipynb` contains CNN, Hyperband, and VGG16 training and evaluation experiments. Model checkpoints are not included; train and save a model before using notebook cells that load one.
