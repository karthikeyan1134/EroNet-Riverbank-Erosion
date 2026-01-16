# EroNet: Spatiotemporal Mapping of Riverbank Erosion & Deposition

**EroNet** is a deep learning-based framework developed to monitor morphodynamics in river systems. Using a **Multi-Channel U-Net** and **NDWI-derived features**, this project classifies riverbank changes into three categories: **Erosion, Deposition, and No Change**. 

The project focuses on a case study of the **Krishna River, Andhra Pradesh, India**, comparing Sentinel-2 satellite imagery from 2016 and 2024.

---

## 🚀 Key Features

* **Lightweight U-Net:** Optimized architecture for semantic segmentation of satellite patches.
* **Feature Engineering:** Utilizes Normalized Difference Water Index (NDWI) to enhance water-land boundary detection.
* **Multi-Class Detection:** Goes beyond binary detection to identify both land loss (erosion) and land gain (deposition).
* **Kaggle Integrated:** Designed to run seamlessly in a Kaggle environment with GPU acceleration.

---

## 🧠 Methodology


The system processes satellite imagery through a multi-step pipeline:
1.  **Preprocessing:** Extraction of 64x64 patches from Sentinel-2 bands.
2.  **Spectral Indices:** Calculation of NDWI to improve feature extraction.
3.  **Segmentation:** Training a U-Net model to generate pixel-wise classification masks.
4.  **Change Detection:** Spatiotemporal comparison of 2016 vs. 2024 masks to map morphological shifts.

---

## 📂 Project Structure (Kaggle Notebook)

Since this project is implemented as a comprehensive Kaggle notebook, the structure is as follows:

* **`urop64patches.ipynb`**: The primary notebook containing data loading, preprocessing, model training, and visualization.
* **Data Input**: Sentinel-2 satellite imagery (TCI and B8 bands).
* **Outputs**: Trained model weights (`.h5`/`.pth`) and generated erosion-deposition maps.

---

## ⚙️ How to Run

### Option 1: Run on Kaggle (Recommended)
1.  Open the notebook on Kaggle: [urop64patches](https://www.kaggle.com/code/sathwik1923/urop64patches)
2.  Click on **"Copy and Edit"**.
3.  Ensure the **Internet** is turned on in the Settings.
4.  Run all cells (`Ctrl + F10`).

### Option 2: Local Execution
1.  Clone this repository:
    ```bash
    git clone [https://github.com/karthikeyan1134/EroNet-Riverbank-Erosion.git](https://github.com/karthikeyan1134/EroNet-Riverbank-Erosion.git)
    ```
2.  Install required libraries:
    ```bash
    pip install numpy pandas matplotlib tensorflow opencv-python
    ```
3.  Open the `.ipynb` file in VS Code or Jupyter Lab.

---

## 📈 Research Context

This project was developed as part of a B.Tech research initiative at **SRM University-AP**. It explores the impact of seasonal floods and human intervention on the Krishna River's path.

**Metrics Achieved:**
* High Precision in NDWI-based water extraction.
* Effective spatial mapping of erosion hotspots near the Krishna River delta.

---

## 🧑‍💻 Author
**Karthikeyan Akkapalli**
* **GitHub**: [@karthikeyan1134](https://github.com/karthikeyan1134)
* **Affiliation**: SRM University-AP, Computer Science & Engineering (Class of 2026)
