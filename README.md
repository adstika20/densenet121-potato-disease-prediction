# 🍂 Deep Learning-Based Classification of Potato Leaf Diseases with DenseNet121

---

## 1. Project Title  
**Deep Learning-Based Classification of Potato Leaf Diseases Using DenseNet121**

---

## 2. Project Description  
This project focuses on detecting and classifying diseases in potato plants through leaf images. The model identifies whether a potato plant is affected by:  
- 🦠 Early Blight  
- 🦠 Late Blight  
- 🌿 Healthy  

The model is trained on a dataset of 1,722 training images, 430 validation images, and 2,152 testing images. It uses DenseNet121 pretrained on ImageNet as backbone, with additional layers like batch normalization, fully connected layers with ReLU activation, dropout, and a softmax output layer for optimized classification.

---

## 3. Results / Preview  
The model was trained for 20 epochs and achieved:  
- 🎯 Training Accuracy: **99.05%**  
- 📉 Training Loss: **0.0573**  
- 🎯 Testing Accuracy: **98.98%**  
- 📉 Testing Loss: **0.0292**  

Training and validation curves show effective learning without overfitting, indicating strong generalization.

![Accuracy and Loss Plot](https://github.com/adstika20/Image-Classification/blob/main/download.png)

---

## 4. 📁 Project Structure  

```
├── data/ # Dataset images and labels
├── models/ # Model architecture and weights
├── notebooks/ # Jupyter notebooks for exploration and training
├── scripts/ # Training and evaluation scripts
├── requirements.txt # Project dependencies
├── README.md # Project documentation
└── utils/ # Utility functions (preprocessing, metrics, etc.)

```

## 5. ⚙️ Installation / Requirements  

Ensure you have **Python 3.7+** installed. Then follow:  

```bash
# Clone the repo
git clone <repo_url>
cd <repo_folder>

# (Optional) Create and activate virtual environment
python -m venv env
source env/bin/activate  # macOS/Linux
env\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt

# Verify TensorFlow installation
python -c "import tensorflow as tf; print(tf.__version__)"

```

## 6. 📦 Dataset

The dataset used in this project is sourced from **Kaggle**:  
[Potato Plant Diseases Dataset](https://www.kaggle.com/datasets/hafiznouman786/potato-plant-diseases-data/data)  

### Dataset Details:  
- Split into three subsets for model training and evaluation:  
  - Training set: 1,722 images  
  - Validation set: 430 images  
  - Testing set: 2,152 images  

This diverse and well-labeled dataset ensures effective training and robust model evaluation.

---

## 7. Methodology

- **Backbone:** Utilized **DenseNet121** pretrained on ImageNet as a powerful feature extractor to capture intricate patterns in leaf images.  
- **Added Layers:**  
  - Batch Normalization to stabilize and accelerate training.  
  - Fully Connected (Dense) layers with ReLU activation to learn complex representations.  
  - Dropout layers to prevent overfitting and improve generalization.  
- **Output Layer:** Softmax activation with 3 neurons to classify input images into the three disease categories.  
- **Training:** Conducted over 20 epochs optimizing categorical cross-entropy loss.  
- **Evaluation:** Model performance validated on a separate test set to ensure accuracy and robustness in real-world conditions.

---

⭐ If you find this project useful, please consider giving it a star!
