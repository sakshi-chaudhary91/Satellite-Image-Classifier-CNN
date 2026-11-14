# 🛰️ Satellite Land Use Classification using CNN (EuroSAT) 

A deep learning project built with **TensorFlow/Keras** to classify land use and land cover types using Sentinel-2 satellite imagery from the **EuroSAT dataset**.   

---

## 📋 Project Overview
Remote sensing and geospatial imaging analysis play a crucial role in environmental monitoring, urban planning, and agriculture. This project implements a Custom Convolutional Neural Network (CNN) from scratch to automatically categorize RGB satellite images into **10 distinct land-use classes**.  

---

## 🗂️ Dataset
* **Dataset Name:** EuroSAT (Land Use and Land Cover Classification with Sentinel-2 Satellite Images)
* **Total Images:** 27,000 labeled RGB images ($64 \times 64$ pixels)
* **Classes (10):**
  1. `AnnualCrop`
  2. `Forest`
  3. `HerbaceousVegetation`
  4. `Highway`
  5. `Industrial`
  6. `Pasture`
  7. `PermanentCrop`
  8. `Residential`
  9. `River`
  10. `SeaLake`

---

## 🏗️ Model Architecture 
The custom CNN pipeline consists of multiple convolutional blocks followed by fully connected layers:
* **Input Layer:** $64 \times 64 \times 3$ (RGB Satellite Images)
* **Conv Blocks:** 3 Convolutional Blocks (Conv2D + ReLU + MaxPooling2D) scaling feature maps up to 128 filters.
* **Classification Head:** Flatten Layer $\rightarrow$ Dense Layer (256 units, ReLU) $\rightarrow$ Dropout (0.4) $\rightarrow$ Dense Output Layer (10 classes with Softmax).
* **Optimizer:** Adam
* **Loss Function:** Sparse Categorical Crossentropy

---

## 📈 Performance & Results
* **Training Accuracy:** ~91.71%
* **Validation Accuracy:** ~87.24%
* **Split Ratio:** 80% Training (21,600 images) / 20% Validation (5,400 images)

---

