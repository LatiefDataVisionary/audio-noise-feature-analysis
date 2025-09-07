# High-Level Speech Feature Analysis of Environmental Noise

[![Python Version](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Project Status](https://img.shields.io/badge/Status-Completed-green.svg)]()

This project is the final capstone for the "High Level Speech Feature" course by BISA AI Academy. It involves extracting, analyzing, and visualizing high-level audio features from a dataset of various environmental noises. The primary features of focus are **Spectrograms** and **Chroma Features**.

---

### **Table of Contents**
1. [Project Overview](#1-project-overview)
2. [Key Features Analyzed](#2-key-features-analyzed)
3. [Dataset](#3-dataset)
4. [Repository Structure](#4-repository-structure)
5. [Installation & Usage](#5-installation--usage)
6. [Sample Visualizations](#6-sample-visualizations)
7. [Tools & Libraries Used](#7-tools--libraries-used)
8. [Author](#8-author)
9. [Acknowledgments](#9-acknowledgments)

---

### **1. Project Overview**

The goal of this project is to apply theoretical knowledge of audio signal processing into practice. By taking a diverse dataset of 10 environmental noises (e.g., rain, traffic, crowded places), we can create a visual "fingerprint" for each sound type. This analysis demonstrates the ability to distinguish different sound characteristics purely through their frequency and pitch class distributions over time.

---

### **2. Key Features Analyzed**

*   🔊 **Spectrogram**: A visual representation of the spectrum of frequencies of a signal as it varies with time. It helps in identifying which frequencies are dominant in a sound.
*   📊 **Chroma Feature (Chromagram)**: A powerful feature that projects the entire spectrum onto 12 bins representing the 12 distinct semitones (or pitch classes) of the musical octave. It is excellent for identifying harmonic content in a sound.

---

### **3. Dataset**

The dataset used is the **Audio Noise Dataset** available on Kaggle. It contains 10 `.webm` audio files of typical background noises recorded in Myanmar.

*   **Source**: [Kaggle Audio Noise Dataset](https://www.kaggle.com/datasets/minsithu/audio-noise-dataset/data)
*   **Content**: 10 audio files capturing noises such as car traffic, rainy days, festivals, and restaurants.

**NOTE**: The dataset is not included in this repository due to its size. Please download it from the source link above to run the analysis. The notebooks assume the data is placed in the appropriate `data/` directory after being converted to `.wav` format.

---

### **4. Repository Structure**

```
Audio-Noise-Feature-Analysis/
├── .gitignore
├── LICENSE
├── README.md
├── requirements.txt
├── notebooks/
│   └── 01_feature_extraction_and_visualization.ipynb
├── reports/
│   └── final_report.pdf
├── data/
│   ├── raw/
│   │   └── .gitkeep
│   └── processed/
│       └── .gitkeep
└── visualizations/
    ├── spectrograms/
    │   └── spectrogram_comparison.png
    └── chroma_features/
        └── chroma_feature_comparison.png
```
---

### **5. Installation & Usage**

To replicate the analysis, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/[Your-Username]/Audio-Noise-Feature-Analysis.git
    cd Audio-Noise-Feature-Analysis
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3.  **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Download the data:**
    Download the dataset from the [Kaggle link](#3-dataset) and place the `.webm` files into the `data/raw/` folder.

5.  **Run the notebook:**
    Open and run the cells in `notebooks/01_feature_extraction_and_visualization.ipynb` to perform the analysis and generate the visualizations.

---

### **6. Sample Visualizations**

Here are some examples of the visualizations generated from the analysis. These plots effectively show the distinct characteristics of each noise type.

**Spectrogram Comparison**
*(Replace this text with your generated comparison plot)*
![Spectrogram Comparison](visualizations/spectrograms/spectrogram_comparison.png)

**Chroma Feature Comparison**
*(Replace this text with your generated comparison plot)*
![Chroma Feature Comparison](visualizations/chroma_features/chroma_feature_comparison.png)

---

### **7. Tools & Libraries Used**

*   **Python 3.9**
*   **Librosa**: For audio and music analysis.
*   **NumPy**: For numerical operations.
*   **Matplotlib & Seaborn**: For data visualization.
*   **Jupyter Notebook / Google Colab**: For interactive development and analysis.
*   **FFmpeg**: For audio format conversion (handled within the notebook).

---

### **8. Author**

*   **[Your Name]** - [Link to your GitHub Profile or LinkedIn]

---

### **9. Acknowledgments**

*   Thanks to **BISA AI Academy** for the comprehensive "High Level Speech Feature" course.
*   Thanks to **Min Si Thu** for providing the audio dataset on Kaggle.
