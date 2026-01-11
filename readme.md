# 🧠 Brain Tumor Prediction using Deep Learning

This project implements an **end-to-end deep learning pipeline** for **brain tumor detection from MRI images** using  **Computer Vision and Attention-based CNNs** .

The goal is to accurately classify brain MRI scans while also ensuring  **model interpretability** , which is critical for medical AI applications.

---

## 📌 Project Overview

Brain tumor detection is a crucial medical imaging task that can assist radiologists and healthcare professionals. In this project, I developed a **transfer learning-based model enhanced with attention mechanisms** to improve both performance and explainability.

Key highlights:

* MRI image preprocessing using **CLAHE**
* **MobileNetV2** with **CBAM attention module**
* **Grad-CAM visualization** for explainable AI
* Complete training, validation, and evaluation pipeline

---

## 🗂️ Dataset Structure

The dataset is organized into three main folders:

<pre class="overflow-visible! px-0!" data-start="1152" data-end="1310"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(--spacing(9)+var(--header-height))] @w-xl/main:top-9"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre!"><span><span>dataset/
│
├── train/
│   ├── tumor/
│   └── no_tumor/
│
├── validation/
│   ├── tumor/
│   └── no_tumor/
│
└── </span><span>test</span><span>/
    ├── tumor/
    └── no_tumor/
</span></span></code></div></div></pre>

Each folder contains MRI images corresponding to their respective class.

---

## ⚙️ Technologies & Libraries Used

* Python
* TensorFlow / Keras
* OpenCV
* NumPy
* Matplotlib
* Scikit-learn

---

## 🔬 Methodology

### 1. Image Preprocessing

* Resized MRI images to a fixed input size
* Applied **CLAHE (Contrast Limited Adaptive Histogram Equalization)** to enhance image contrast
* Normalized pixel values

### 2. Model Architecture

* Used **MobileNetV2** as the base model (pretrained on ImageNet)
* Integrated **CBAM (Convolutional Block Attention Module)** to improve feature focus
* Added custom fully connected layers for classification

### 3. Training Strategy

* Transfer learning with frozen base layers
* Fine-tuning for better domain adaptation
* Optimized using Adam optimizer
* Binary cross-entropy loss function

### 4. Model Evaluation

* Accuracy and loss curves
* Classification report
* Confusion matrix

### 5. Explainable AI

* Implemented **Grad-CAM** to visualize important regions in MRI scans
* Helps validate whether the model is focusing on tumor-affected areas

---

## 📊 Results

* The attention-based model demonstrated improved feature learning
* Grad-CAM visualizations confirmed meaningful focus on tumor regions
* Achieved stable convergence with minimal overfitting

*(Exact metrics can be added here if required)*

---

## 📈 Key Learnings

* Attention mechanisms enhance CNN performance and interpretability
* Preprocessing is critical in medical imaging tasks
* Explainability is essential for trust in healthcare AI systems
* Transfer learning significantly reduces training time while maintaining accuracy

---

## 🚀 Future Improvements

* Extend to **multi-class tumor classification**
* Experiment with different attention mechanisms
* Hyperparameter tuning for better performance
* Deployment using Streamlit or FastAPI

---

## 📁 How to Run the Project

1. Clone the repository:

<pre class="overflow-visible! px-0!" data-start="3249" data-end="3287"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(--spacing(9)+var(--header-height))] @w-xl/main:top-9"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre! language-bash"><span><span>git </span><span>clone</span><span> <repository_url>
</span></span></code></div></div></pre>

2. Install dependencies:

<pre class="overflow-visible! px-0!" data-start="3314" data-end="3357"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(--spacing(9)+var(--header-height))] @w-xl/main:top-9"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre! language-bash"><span><span>pip install -r requirements.txt
</span></span></code></div></div></pre>

3. Run the notebook:

<pre class="overflow-visible! px-0!" data-start="3380" data-end="3437"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(--spacing(9)+var(--header-height))] @w-xl/main:top-9"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre! language-bash"><span><span>jupyter notebook Brain_Tumor_Prediction.ipynb
</span></span></code></div></div></pre>

---

## 🤝 Contribution

Contributions, suggestions, and feedback are welcome!

Feel free to fork the repository or open an issue.
