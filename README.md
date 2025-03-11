# Land Type Classification Using EuroSAT Dataset

## Overview

This project focuses on classifying land types using the EuroSAT dataset, which contains satellite images captured by the Sentinel-2A satellite. The dataset includes images from 10 distinct land categories, such as "Forest," "River," and "Residential." The goal is to train a model to classify these land types based on image features.

## Dataset

- **Source:** [EuroSAT dataset on Kaggle](https://www.kaggle.com/datasets/nilesh789/eurosat-rgb)
- **Size:** 27,000+ images
- **Resolution:** 64x64 pixels
- **Captured By:** Sentinel-2A satellite
- **Classes:** 10 distinct land categories (e.g., Forest, River, Residential)

### Dataset Access

To access the dataset, you can either:

- **Download via Kaggle API:**

  You'll need your Kaggle API token for this method.

  ```bash
  kaggle datasets download -d nilesh789/eurosat-rgb
  ```

  Make sure to place your Kaggle API token file in the correct directory (usually `~/.kaggle/kaggle.json`).

- **Manual Download:**
  
  You can also manually download the dataset from the Kaggle page [EuroSAT dataset](https://www.kaggle.com/datasets/nilesh789/eurosat-rgb) and extract the files to the project directory.

## Project Structure

- **`notebooks/`**: Contains Jupyter notebooks with additional exploratory data analysis and model development steps.

## Key Steps in the Project

1. **Data Exploration and Visualization:**
   - The dataset is first explored to understand class distributions and RGB channel statistics.
   - Visualize the image classes and check for any class imbalance, especially the underrepresented "Pasture" class.
   
2. **Preprocessing:**
   - The FastAI `DataBlock` API is used to preprocess the dataset, including image resizing and augmentation for training.
   - Class balancing techniques like resampling or using a weighted loss function are suggested for better model performance, especially for underrepresented classes like "Pasture."

3. **Model Training:**
   - The dataset is split into training and validation sets (80%/20% split).
   - Augmentation techniques like rotation, flipping, and cropping are applied to improve model generalization.

## Requirements

To run this project, you need to install the following dependencies:

- `fastai`
- `torch`
- `opencv-python`
- `seaborn`
- `matplotlib`

You can install these packages via pip:

```bash
pip install fastai torch opencv-python seaborn matplotlib
```

## License

This project is licensed under the MIT License.

## Acknowledgments

- The EuroSAT dataset is provided by Kaggle and is a useful resource for land type classification problems.
- Thanks to FastAI for providing a convenient API for data processing and model training.
