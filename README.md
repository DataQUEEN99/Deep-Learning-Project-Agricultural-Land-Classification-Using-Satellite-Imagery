
# Agricultural Land Classification Using Satellite Imagery

## Deep Learning and Computer Vision | Coursera Project

An end-to-end deep learning project for classifying agricultural and non-agricultural land using satellite imagery. This project explores CNNs, Vision Transformers, and a hybrid CNN + ViT architecture to understand how different deep learning approaches perform on remote sensing image classification.

---

## Project Overview

Agricultural land classification is an important application of remote sensing and artificial intelligence. Automatically identifying agricultural regions from satellite imagery can support agricultural monitoring, land-use analysis, and data-driven environmental planning.

This project develops and evaluates deep learning models that classify satellite images into two categories:

- Agricultural Land
- Non-Agricultural Land

The project was completed as a hands-on Coursera deep learning project, applying concepts from computer vision, model development, and machine learning evaluation.

---

## Objectives

- Develop an end-to-end satellite image classification pipeline.
- Explore CNN-based image classification.
- Implement and compare TensorFlow/Keras and PyTorch models.
- Experiment with Vision Transformer architectures.
- Develop a hybrid CNN + Vision Transformer model.
- Evaluate model performance using multiple classification metrics.
- Analyze model errors and prediction behavior.
- Apply explainability techniques to understand model decisions.
- Document the complete deep learning workflow.

---

## Technologies and Tools

| Category | Technologies |
|---|---|
| Programming | Python |
| Deep Learning | TensorFlow, Keras, PyTorch |
| Computer Vision | CNN, Vision Transformer |
| Data Processing | NumPy, Pandas |
| Image Processing | PIL, OpenCV |
| Visualization | Matplotlib, Seaborn |
| Evaluation | Scikit-learn |
| Development | Jupyter Notebook / Google Colab |
| Domain | Remote Sensing and Agriculture |

---

## Dataset

The project uses satellite imagery labeled into agricultural and non-agricultural land classes.

### Classification Classes

| Class | Description |
|---|---|
| Agricultural Land | Satellite images representing agricultural regions |
| Non-Agricultural Land | Satellite images representing non-agricultural regions |

### Dataset Preparation

The dataset preparation workflow includes:

1. Loading the image dataset.
2. Inspecting class distribution.
3. Checking image dimensions and quality.
4. Visualizing representative samples.
5. Preprocessing images for model input.
6. Splitting data into training, validation, and testing sets.

> Note: Add the original dataset name, source link, number of images, image dimensions, and license here before publishing the repository.

---

## Project Workflow

```text
Satellite Image Dataset
          |
          v
Data Loading and Exploration
          |
          v
Image Preprocessing
          |
          v
Data Augmentation
          |
          v
Train / Validation / Test Split
          |
          v
+-----------------------------+
| Deep Learning Architectures |
+-----------------------------+
          |
    +-----+-----+-------------+
    |           |             |
    v           v             v
 Keras CNN  PyTorch CNN     ViT
    |           |             |
    +-----------+-------------+
                |
                v
       CNN + ViT Hybrid
                |
                v
       Model Evaluation
                |
                v
  Explainability and Error Analysis
                |
                v
       Final Documentation
```

---

## Deep Learning Models

### 1. Keras CNN

A convolutional neural network implemented using TensorFlow/Keras.

CNNs are effective for image classification because they learn spatial features such as edges, textures, shapes, and patterns.

**Workflow:**

```text
Input Image
    |
Convolution Layers
    |
Pooling Layers
    |
Feature Extraction
    |
Fully Connected Layers
    |
Classification Output
```

### 2. PyTorch CNN

A CNN implementation using PyTorch to explore model development and training in a different deep learning framework.

This comparison helped strengthen understanding of:

- Model architecture design
- Training loops
- Loss functions
- Optimizers
- Backpropagation
- Validation and testing

### 3. Vision Transformer (ViT)

The Vision Transformer processes images using image patches and self-attention mechanisms.

Instead of relying exclusively on convolutional operations, ViT learns relationships between image patches to capture broader spatial patterns.

**Key concepts:**

- Image patch extraction
- Patch embeddings
- Positional embeddings
- Self-attention
- Transformer encoder blocks
- Classification head

### 4. CNN + Vision Transformer Hybrid

The hybrid model combines convolutional feature extraction with transformer-based representation learning.

The CNN extracts local spatial features, while the transformer helps model relationships across image regions.

The hybrid architecture achieved the strongest performance among the evaluated models in this project’s test results.

> Important: The exact performance values should be added from the final evaluation notebook.

---

## Data Preprocessing

The preprocessing pipeline includes:

- Image loading and validation.
- Resizing images to the model input dimensions.
- Pixel normalization.
- Label encoding.
- Dataset splitting.
- Batch preparation.

### Data Augmentation

Augmentation was used to improve training diversity and help reduce overfitting.

Possible transformations include:

- Random horizontal and vertical flips.
- Small image rotations.
- Random crops or resized crops.
- Brightness and contrast adjustments.

Augmentation should be applied only to the training set, while validation and test images should use consistent evaluation preprocessing.

---

## Model Training

The training pipeline includes:

1. Initialize the model.
2. Define the classification loss function.
3. Configure the optimizer.
4. Train on the training dataset.
5. Evaluate on the validation dataset.
6. Track training and validation metrics.
7. Apply regularization or early stopping when appropriate.
8. Save the best-performing model checkpoint.

### Training Monitoring

The project analyzes:

- Training loss.
- Validation loss.
- Training accuracy.
- Validation accuracy.
- Signs of overfitting.
- Model convergence.

---

## Model Evaluation

The models were evaluated using multiple performance metrics rather than accuracy alone.

### Accuracy

Measures the proportion of correctly classified images.

### Precision

Measures how many images predicted as agricultural land were actually agricultural land.

### Recall

Measures how many actual agricultural images were correctly identified.

### F1-Score

Combines precision and recall into a single metric.

### ROC-AUC

Measures the model’s ability to distinguish between the two classes across classification thresholds.

### Confusion Matrix

Provides a detailed view of:

- True Positives
- True Negatives
- False Positives
- False Negatives

---

## Visualization and Analysis

The project includes the following visual analyses:

### Dataset Exploration

- Class distribution.
- Sample satellite images.
- Image dimensions.
- Label balance.

### Training Analysis

- Training and validation accuracy curves.
- Training and validation loss curves.
- Learning behavior across epochs.

### Classification Analysis

- Confusion matrices.
- ROC curves.
- Precision and recall comparison.
- F1-score comparison.
- Model performance comparison charts.

### Prediction Error Analysis

Incorrect predictions were analyzed to understand potential challenges such as:

- Similar visual patterns between classes.
- Mixed land-use regions.
- Image quality variations.
- Seasonal differences.
- Complex landscape structures.

---

## Explainable AI

Model explainability was explored to better understand which image regions influence predictions.

Potential explainability methods include:

- Grad-CAM for CNN-based models.
- Attention visualization for transformer-based models.
- Saliency-based image analysis.

These techniques can help identify whether models focus on meaningful landscape features or irrelevant visual patterns.

> Explainability results should be interpreted carefully. Highlighted regions indicate model sensitivity, not proof of causal reasoning.

---

## Results

The CNN + Vision Transformer hybrid model achieved the strongest performance among the evaluated architectures in the project’s test results.

### Model Comparison

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---|---|---|---|---|
| Keras CNN | Add result | Add result | Add result | Add result | Add result |
| PyTorch CNN | Add result | Add result | Add result | Add result | Add result |
| Vision Transformer | Add result | Add result | Add result | Add result | Add result |
| CNN + ViT Hybrid | Add result | Add result | Add result | Add result | Add result |

**Best-performing architecture:** CNN + Vision Transformer Hybrid

> Replace the placeholder values with the actual test-set metrics from your notebook. Do not report estimated or unverified performance values.

---

## Project Structure

```text
agricultural-land-classification/
│
├── README.md
├── notebooks/
│   └── agricultural_land_classification.ipynb
│
├── data/
│   ├── train/
│   ├── validation/
│   └── test/
│
├── models/
│   ├── keras_cnn/
│   ├── pytorch_cnn/
│   ├── vision_transformer/
│   └── cnn_vit_hybrid/
│
├── results/
│   ├── training_curves/
│   ├── confusion_matrices/
│   ├── roc_curves/
│   ├── model_comparison/
│   └── explainability/
│
├── requirements.txt
└── .gitignore
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/agricultural-land-classification.git
cd agricultural-land-classification
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Example requirements:

```text
numpy
pandas
matplotlib
seaborn
scikit-learn
tensorflow
torch
torchvision
pillow
opencv-python
jupyter
```

> Use a compatible TensorFlow and PyTorch installation for your hardware and Python version.

---

## How to Run

### Option 1: Google Colab

1. Open the notebook in Google Colab.
2. Upload or connect the dataset.
3. Install the required dependencies.
4. Run the preprocessing cells.
5. Train the selected models.
6. Evaluate the models.
7. Review the visualizations and final results.

### Option 2: Local Jupyter Notebook

```bash
jupyter notebook
```

Open the project notebook and execute the cells in order.

---

## Key Learnings

This project strengthened my understanding of:

- End-to-end deep learning workflows.
- Satellite image classification.
- CNN architecture development.
- Vision Transformer experimentation.
- Hybrid deep learning architectures.
- Model evaluation beyond accuracy.
- Overfitting detection and prevention.
- Explainable AI.
- Error analysis.
- Scientific documentation and communication.

A major takeaway was that successful deep learning projects require more than training a model. Dataset quality, architecture selection, evaluation methodology, and interpretation of results are equally important.

---

## Future Improvements

Potential improvements include:

- Training on a larger and more diverse satellite imagery dataset.
- Using pretrained CNN and Vision Transformer backbones.
- Applying transfer learning.
- Conducting hyperparameter optimization.
- Exploring multispectral satellite data.
- Evaluating performance across different geographic regions.
- Adding land-cover segmentation.
- Developing a web-based prediction application.
- Deploying the best model using FastAPI or Streamlit.
- Investigating model robustness under seasonal and geographic shifts.

---

## Applications

This type of classification system can support research and development in:

- Agricultural monitoring.
- Land-use classification.
- Remote sensing analysis.
- Environmental monitoring.
- Geospatial AI.
- Precision agriculture.
- Land-cover mapping.

The project is an educational deep learning classification study and should not be treated as a validated operational land-monitoring system without further geographic and field-level evaluation.

---

## Author

**Kushi Kumari**

BSc Bioinformatics, Statistics and Data Science

### Interests

- Artificial Intelligence
- Machine Learning
- Deep Learning
- Computer Vision
- Remote Sensing
- Large Language Models
- RAG and Agentic AI

---

## Acknowledgements

This project was completed as part of a hands-on Coursera deep learning learning experience.

Thanks to the Coursera learning platform and course instructors for providing the foundation and practical concepts used in this project.

---

## License

Add an appropriate license based on the dataset terms and your project requirements.

---

## Project Status

Completed — Deep Learning and Computer Vision Project

The project includes model development, architecture comparison, evaluation, visualization, and documentation.
