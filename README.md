# 🧠 Glass Crack & Defect Detection using CNN

This project classifies various defects in glass (e.g. cracks, scratches, spots, blotches) using a **Convolutional Neural Network (CNN)** trained on the [SSGD dataset](https://github.com/weiji14/SSGD). It maps detailed defect classes to broader **crack severity levels**, enabling real-world fault analysis.

---

## 🔍 Features

- 📦 Uses XML annotations from multiple folders (`lb101`, `lb201`) in the SSGD dataset
- 🧠 Classifies images into one of the following:
  - `no_crack`
  - `small_crack`
  - `heavy_crack`
- 🎯 Achieved **83.78% test accuracy**
- 🏆 Uses **EarlyStopping** and **ModelCheckpoint** for optimal training
- 📊 Visualized model evaluation via `classification_report` and `confusion_matrix`

---

## 🧰 Tech Stack

| Tool/Library | Purpose |
|--------------|---------|
| Python 3.x   | Core language |
| TensorFlow / Keras | Deep learning framework |
| PIL, OpenCV  | Image processing |
| Matplotlib   | Visualization |
| XML + ElementTree | Dataset annotation parsing |
| Scikit-learn | Evaluation & splitting |

---

## 🧾 Class Mapping

From raw labels to simplified classification:

| Raw Label         | Mapped Defect    | Severity     |
|-------------------|------------------|--------------|
| `huahen`          | scratch          | small_crack  |
| `liewen`          | crack            | heavy_crack  |
| `baidian`         | spot             | small_crack  |
| `louguang`        | light-leakage    | small_crack  |
| `bengque`         | broken           | heavy_crack  |
| `wuzi`            | blot             | small_crack  |
| `pomo`            | broken-membrane  | heavy_crack  |
| `ok`              | no-defect        | no_crack     |

---

## 📂 Folder Structure

glass-crack-detection-main/
├── data/ # Parsed dataset
├── train.py # Model training script
├── test.py # Evaluation logic
├── ssgd_parser.py # Parses XML annotations
├── utils.py # Image utils (resizing, augmenting)
├── requirements.txt
└── README.md

---


