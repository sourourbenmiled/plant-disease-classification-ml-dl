# 🌿 Plant Disease Detection & Classification

**An end-to-end Computer Vision and Artificial Intelligence project for automatic plant leaf disease detection and classification using Machine Learning and Deep Learning.**

## 📌 Overview

This project explores different Artificial Intelligence approaches to identify plant diseases from leaf images.

Using the **PlantVillage dataset**, the notebook implements a complete image classification pipeline, from image preprocessing and segmentation to feature extraction, model training, and performance evaluation.

The project compares traditional Machine Learning algorithms with Deep Learning models based on Transfer Learning to investigate their effectiveness in plant disease classification.

## 🎯 Objectives

- Explore and visualize plant leaf image datasets.
- Apply image preprocessing and normalization techniques.
- Perform image segmentation and edge detection.
- Extract color, texture, and shape features.
- Train and evaluate traditional Machine Learning classifiers.
- Implement Transfer Learning using pretrained CNN architectures.
- Compare ML and DL approaches using classification metrics.

## 📊 Dataset

**PlantVillage Dataset**

- Approximately 54,000 images.
- 38 original classes.
- 8 selected classes covering 3 plant types.

### Selected Plant Categories

| Plant | Classes |
|---|---|
| 🥔 Potato | Early Blight, Late Blight, Healthy |
| 🍅 Tomato | Early Blight, Late Blight, Healthy |
| 🫑 Pepper | Bacterial Spot, Healthy |

The selected dataset contains both healthy and diseased leaves, allowing the models to distinguish between different plant health conditions.

## ⚙️ Project Pipeline

The notebook is organized into the following phases:

### 1. Dataset Exploration
- Dataset inspection and visualization.
- Class distribution analysis.
- Selection of 8 disease categories.

### 2. Image Preprocessing
- Image resizing (128×128 and 224×224).
- RGB and HSV color space conversion.
- Grayscale transformation.
- Gaussian filtering.
- Pixel normalization.

### 3. Image Segmentation & Edge Detection

Several techniques are explored:
- Sobel edge detection.
- Canny edge detection.
- Otsu thresholding.
- HSV-based segmentation.
- K-means clustering.

### 4. Feature Extraction

Manual feature engineering combines:

- **Color features:** RGB and HSV histograms.
- **Texture features:** Gray-Level Co-occurrence Matrix (GLCM).
- **Shape features:** Area, perimeter, and circularity.

### 5. Traditional Machine Learning

Two classification algorithms are implemented:

| Algorithm | Configuration |
|---|---|
| SVM | RBF kernel, C=10 |
| Random Forest | 200 estimators |

Feature scaling is performed using StandardScaler.

### 6. Deep Learning – Transfer Learning

Three pretrained CNN architectures are compared:

| Model | Architecture |
|---|---|
| MobileNetV2 | Lightweight CNN |
| ResNet50 | Residual Neural Network |
| EfficientNetB0 | Efficient CNN architecture |

Each model uses a two-stage training strategy:

1. Feature extraction with frozen pretrained layers.
2. Fine-tuning with partially unfrozen layers.

Data augmentation is also applied to improve model generalization.

### 7. Model Evaluation & Comparison

Models are evaluated using:

- Accuracy
- Precision
- Recall
- Confusion matrices
- Training and validation accuracy
- Training and validation loss

The final phase compares traditional ML algorithms with Deep Learning approaches.

## 🛠️ Technologies & Libraries

| Technology | Purpose |
|---|---|
| Python | Programming language |
| OpenCV | Image processing |
| NumPy & Pandas | Data manipulation |
| Scikit-image | Texture and region analysis |
| Scikit-learn | Machine Learning |
| TensorFlow / Keras | Deep Learning |
| Matplotlib & Seaborn | Data visualization |

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/plant-disease-classification-ml-dl.git
cd plant-disease-classification-ml-dl
```

### 2. Install dependencies

```bash
pip install numpy pandas matplotlib seaborn
pip install opencv-python scikit-image scikit-learn
pip install tensorflow
pip install jupyter
```

### 3. Download the dataset

Download the PlantVillage dataset from Kaggle:

https://www.kaggle.com/datasets/emmarex/plantdisease

Extract the dataset and update the `BASE_DIR` variable in the notebook to point to the `PlantVillage` directory.

### 4. Run the notebook

```bash
jupyter notebook
```

Open the project notebook and execute the cells sequentially.

**Note:** Deep Learning training requires additional computational resources. GPU acceleration is recommended.

## 📈 Key Takeaways

This project demonstrates the differences between traditional Machine Learning and Deep Learning in image classification.

- Traditional ML relies on manually engineered color, texture, and shape features.
- Deep Learning automatically learns visual representations from images.
- Transfer Learning allows pretrained architectures to adapt to plant disease classification.
- Model comparison helps identify the trade-off between classification performance and computational efficiency.

## ⚠️ Limitations

The PlantVillage dataset primarily contains images captured under controlled conditions with relatively uniform backgrounds.

Consequently, model performance on real-world field images may differ. Predictions should be considered experimental and not a substitute for professional agricultural diagnosis.

## 👩‍💻 Author

**Your Name**

Computer Engineering Student | Software Engineering | Artificial Intelligence & Machine Learning

---

⭐ If you find this project interesting, feel free to star the repository!
