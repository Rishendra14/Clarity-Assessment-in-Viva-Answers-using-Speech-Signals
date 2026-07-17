🎙️ Clarity Assessment in Viva Answers using Speech Signals
A Machine Learning and Speech Processing project for automatically assessing the clarity of students' viva responses using speech signal features.


📖 Overview

This project aims to automatically assess the **clarity of students' viva voce answers** using speech signal processing and machine learning techniques.
Instead of evaluating only the spoken content, the system analyzes the **acoustic properties** of speech and classifies each student's response into one of the following clarity levels:
- 🟢 High
- 🟡 Medium
- 🔴 Low
The project also explores **spectrogram-based deep learning models** and compares their performance with traditional speech feature-based machine learning models.


🎯 Objectives

- Develop an automated system for viva clarity assessment.
- Build a custom labelled speech dataset.
- Extract meaningful speech features.
- Train and compare multiple machine learning models.
- Evaluate model performance using standard classification metrics.


📂 Dataset Creation

Since no publicly available dataset existed for this problem, a **custom dataset** was created through multiple stages.

1️⃣ Collection of Viva Recordings

- Collected multiple real viva examination recordings.
- Each recording contained conversations between **students and teachers**.

2️⃣ Manual Speech Annotation

Using **Praat**, every recording was manually analyzed.

Each speech segment was labelled as:

- 👨‍🎓 Student
- 👨‍🏫 Teacher

Only the **student speech segments** were retained for further analysis.

3️⃣ Dataset Preparation

After extracting student speech,

- Individual student audio clips were created.
- Metadata for each sample was stored in an Excel sheet.
- Every student response was manually labelled as:

| Label | Description |
|--------|-------------|
| 🟢 High | Clear and fluent speech |
| 🟡 Medium | Moderately clear speech |
| 🔴 Low | Poor clarity |

This labelled dataset served as the ground truth for model training and evaluation.


🎵 Speech Feature Extraction

For every labelled student audio sample, the following speech features were extracted:

| Feature | Purpose |
|----------|---------|
| **MFCC** | Captures perceptually important spectral characteristics of speech |
| **LPC** | Models the vocal tract and speech production mechanism |
| **DCT** | Provides compact frequency-domain representation |

The extracted features were converted into structured CSV datasets for machine learning.



🔄 Project Workflow


Viva Audio Recordings
        │
        ▼
Manual Annotation (Praat)
(Student / Teacher)
        │
        ▼
Student Audio Extraction
        │
        ▼
Manual Clarity Labelling
(High / Medium / Low)
        │
        ▼
Speech Feature Extraction
(MFCC • LPC • DCT)
        │
        ▼
Feature Dataset (CSV)
        │
        ▼
Data Preprocessing
        │
        ▼
Machine Learning Models
        │
        ▼
Clarity Prediction



🤖 Machine Learning Models

The following traditional machine learning models were trained and evaluated using the extracted speech features:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest
- AdaBoost
- XGBoost
- CatBoost
- Multi-Layer Perceptron (MLP)


🧠 Deep Learning Models

For comparison, spectrogram images generated from audio signals were also used to train several CNN-based architectures.

- VGG16
- AlexNet
- MobileNetV2
- DenseNet121
- Custom CNN
- Shallow CNN

 
🛠️ Technologies Used

| Category | Tools |
|----------|-------|
| Programming | Python |
| Audio Processing | Praat, Librosa |
| Data Analysis | NumPy, Pandas |
| Machine Learning | Scikit-learn |
| Deep Learning | TensorFlow, Keras |
| Visualization | Matplotlib, Seaborn |
| Development | Jupyter Notebook, Google Colab |


📁 Repository Structure


Clarity-Assessment/
│
├── notebooks/
│   ├── Feature Extraction
│   ├── Machine Learning
│   └── Deep Learning
│
├── feature_csv/
│   ├── mfcc_mean_features.csv
│   ├── lpc_mean_features.csv
│   └── dct_mean_features.csv
│
├── deep_learning/
│
├── results/
│
├── images/
│
├── README.md
├── requirements.txt
└── .gitignore



📊 Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Classification Report


📈 Results

The project compares both **traditional machine learning** and **deep learning** approaches for clarity assessment.

- Traditional ML models were trained using **MFCC, LPC, and DCT** features.
- Deep learning models were trained using **spectrogram images**.
- Performance was compared using standard classification metrics to identify the most effective approach.




