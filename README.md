# High-Level Speech Feature Analysis of Environmental Noise

[![Python Version](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Project Status](https://img.shields.io/badge/Status-Completed-green.svg)]()

### **Project Abstract**
This repository contains the final capstone project for the BISA AI Academy's "High Level Speech Feature" course. It presents a deep dive into the world of audio signal processing by transforming invisible sound waves into rich, visual data. By extracting and visualizing **Spectrograms** and **Chroma Features** from a diverse dataset of 10 environmental noises, this project demonstrates how to uncover the unique "fingerprint" of each sound, laying the foundational groundwork for advanced applications in audio classification, analysis, and machine learning.

---

### **Table of Contents**
1. [Project Motivation](#1-project-motivation)
2. [Key Features Analyzed](#2-key-features-analyzed)
3. [The Dataset](#3-the-dataset)
4. [Key Insights & Observations](#4-key-insights--observations)
5. [Visual Evidence: The Final Plots](#5-visual-evidence-the-final-plots)
6. [Potential Applications](#6-potential-applications)
7. [Repository Structure](#7-repository-structure)
8. [Getting Started: Installation & Usage](#8-getting-started-installation--usage)
9. [Technology Stack](#9-technology-stack)
10. [Author](#10-author)
11. [Acknowledgments](#11-acknowledgments)

---

### **1. Project Motivation**
In an increasingly noisy world, the ability to automatically understand and differentiate sounds is critical. From urban planning to environmental monitoring and smart home devices, identifying the source and nature of audio is a key challenge. This project tackles this challenge by asking a fundamental question: *Can we visually distinguish different types of environmental noise solely based on their spectral properties?* The goal is to prove that by applying signal processing techniques, we can create powerful visual representations that make the characteristics of each sound immediately apparent.

---

### **2. Key Features Analyzed**

To achieve our goal, we focused on two powerful high-level audio features:

*   🔊 **Spectrogram**: A visual masterpiece that maps the frequency content of a signal over time. It allows us to see the distribution of energy across different frequency bands, revealing everything from the low rumble of traffic to the high-pitched buzz of a mosquito.
*   📊 **Chroma Feature (Chromagram)**: Traditionally a tool for music analysis, a chromagram projects the audio's energy onto the 12 pitch classes of the musical scale. Its application to environmental noise is an exploratory move to detect hidden harmonic content—like background music in a festival or the whine of machinery—that spectrograms alone might not highlight.

---

### **3. The Dataset**

The analysis is performed on the **Audio Noise Dataset**, an excellent collection of real-world sounds.

*   **Source**: [Kagle Audio Noise Dataset by Min Si Thu](https://www.kaggle.com/datasets/minsithu/audio-noise-dataset/data)
*   **Content**: Contains 10 audio clips capturing distinct environmental noises, including `Car Traffic`, `Rainy Day`, `Festival`, `Restaurant`, and more.

**Note**: The dataset is not included in this repository. To reproduce the analysis, please download it from the source link and place it in the designated data folder as per the instructions in the notebook.

---

### **4. Key Insights & Observations**

The visual analysis yielded clear and compelling results, confirming our hypothesis.

#### **Spectrogram Analysis: Uncovering the Audio Fingerprint**

The spectrogram was exceptionally effective at revealing the unique time-frequency signature of each noise source.

*   **Distinct Frequency Signatures:** Every noise category showcased a unique pattern.
    *   **Low-Frequency Dominance:** Sounds like `Car Traffic` and `Motorbike and People Talking` exhibited a dense concentration of energy in the low-frequency bands (<1000 Hz), perfectly visualizing the characteristic rumble of engines.
    *   **Broadband Consistency:** Ambient sounds like a `Rainy Day` displayed broadband characteristics, appearing as a uniform, static-like texture across the entire frequency spectrum, indicating energy spread without a strong tonal center.
    *   **Human Activity Hubs:** Noises from `A Crowded Place` and `The Restaurant` showed complex energy patterns primarily in the mid-to-high frequency ranges (1-5 kHz), consistent with the spectral footprint of human speech and general commotion.
    *   **Transient Events:** The `Painful Sounds` category was identifiable by sharp, vertical lines spanning a wide frequency range—the classic sign of sudden, high-energy events like impacts or sharp cries.

#### **Chroma Feature Analysis: Detecting Hidden Harmonics**

While less intuitive for noise, the chromagram provided a valuable secondary layer of analysis.

*   **Revealing Musicality:** The `Festival` noise stood out dramatically. Its chromagram showed strong, stable horizontal bands, providing undeniable evidence of musical elements (e.g., a bassline or melody) within the ambient recording.
*   **The Signature of Atonality:** For most non-tonal noises (`Car Traffic`, `Rain`, `Mosquitos`), the chromagram showed a diffuse, washed-out energy distribution across all 12 pitch classes. This "lack of pattern" is itself a powerful feature for identifying purely ambient or mechanical sounds.
*   **A Complementary View:** This confirms that chroma features, while specialized, can successfully complement spectrograms by acting as a "harmonic content detector," helping to differentiate complex soundscapes.

---

### **5. Visual Evidence: The Final Plots**

A picture is worth a thousand words. The following plots, generated by the analysis notebook, provide a side-by-side comparison that visually summarizes the findings above.

**Comparative Analysis of Audio Features (Spectogram VS Chroma)**
![Comparative Analysis of Audio Features](reports/Comparative%20Analysis%20of%20Audio%20Features.png)

---

### **6. Potential Applications**

The techniques and findings from this project form a robust foundation for numerous real-world applications, including:

*   **Urban Soundscape Monitoring:** Deploying sensors in smart cities to automatically classify noise sources (traffic, construction, social gatherings) for noise pollution analysis.
*   **Anomaly Detection:** Building security or industrial maintenance systems that listen for unusual sounds (e.g., breaking glass, machinery malfunction) which would have a distinct spectral signature.
*   **Bioacoustics:** Applying similar feature extraction methods to classify animal sounds for ecological monitoring and biodiversity studies.
*   **Context-Aware Systems:** Enabling devices to adapt their behavior based on the ambient noise environment (e.g., a phone automatically adjusting its ringer volume).

---

### **7. Repository Structure**

A clean and organized structure is maintained for clarity and reproducibility.
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
│   └── .gitkeep
└── visualizations/
    ├── spectrogram_comparison.png
    └── chroma_feature_comparison.png
```

---

### **8. Getting Started: Installation & Usage**

Follow these steps to replicate the analysis on your own machine.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/[Your-Username]/Audio-Noise-Feature-Analysis.git
    cd Audio-Noise-Feature-Analysis
    ```

2.  **Set up a Python virtual environment (highly recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use: venv\Scripts\activate
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Download the dataset** from the [Kaggle link](#3-the-dataset) and place the audio files in a location accessible by your notebook (e.g., a `data/raw` folder).

5.  **Launch the notebook** in the `notebooks/` directory and run the cells sequentially to perform the analysis.

---

### **9. Technology Stack**

*   **Core Language:** **Python 3.9+**
*   **Audio Processing:** **Librosa**
*   **Numerical Computation:** **NumPy**
*   **Data Visualization:** **Matplotlib & Seaborn**
*   **Development Environment:** **Google Colab / Jupyter Notebook**
*   **Audio Conversion:** **FFmpeg**

---

### **10. Author**

*   **[Nama Anda]** - Feel free to connect! [[GitHub Profile]](https://github.com/your-username) | [[LinkedIn Profile]](https://www.linkedin.com/in/your-profile/)

---

### **11. Acknowledgments**

*   This project was made possible by the excellent curriculum and guidance from the **BISA AI Academy**.
*   Special thanks to **Min Si Thu** for curating and sharing the environmental noise dataset.
