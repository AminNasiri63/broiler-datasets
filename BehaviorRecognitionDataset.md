# Broiler Behavior Recognition Dataset
This dataset includes different videos of various broilers’ behaviors gathered to train a **video classifier model**. The collected videos were manually classified into three classes: **preening**, **stretching**, and **normal**. The **preening** class contains frames where a broiler preens its feathers with its beak; the **stretching** class includes frames where a broiler stretches one wing and one leg; and the **normal** class represents other broiler behaviors such as sitting, standing, feeding, and drinking. To enhance the accuracy of the video classifier model’s results, efforts were made to ensure that each video contained only one broiler. All videos were recorded from **commercial farms** using a **top-view camera** setup.

The dataset was created to support research in:
* Automated detection and classification broiler behaviors.
* Video recognition-based pipeline to detect and quantify the broilers’ behaviors.
* Welfare monitoring.

---

# 🗄️ Dataset Contents
This dataset contains annotated broiler videos classified into behavioral categories:

| Behavior Class | Number of Videos | Video Format | Resolution (pixels) |
|----------------|------------------|--------------|---------------------|
| Normal         | 501              | MP4          | 150 × 150           |
| Preening       | 502              | MP4          | 150 × 150           |
| Stretching     | 516              | MP4          | 150 × 150           |

---

# 🗂️ Data Structure

```
📁 BehaviorRecognition/
│
└── 📁 Normal/
    ├── 📄 N0.mp4
    ├── 📄 N1.mp4
    └── ...

└── 📁 Preening/
    ├── 📄 P0.mp4
    ├── 📄 P1.mp4
    └── ...

└── 📁 Stretching/
    ├── 📄 S0.mp4
    ├── 📄 S1.mp4
    └── ...

```

---


# 📑 Data Summary
| Attribute            | Value    |
| -------------------- | -------- |
| Number of classes    | 3        |
| Total videos         | 1,519    |
| video resolution     | 150×150  |
| Video format         | mp4      |

---

## 📥 Dataset Download

You can directly download the dataset Download from: [![Download Dataset](https://img.shields.io/badge/Download-Dataset-blue)](https://www.ut-smartagriculture.com/datasets/broiler-behavior-recognition-dataset)


---

# 📚 Citation
If you use this dataset, please cite:

```
Nasiri, A., Zhao, Y. and Gan, H., 2024. Automated detection and counting of broiler behaviors using a video recognition system. Computers and Electronics in Agriculture, 221, p.108930.
DOI: https://doi.org/10.1016/j.compag.2024.108930
```

---

# ✉️ Contact
* **Name**: Hao Gan -- Amin Nasiri
* **Email**: hgan1@utk.edu -- aminnassiri63@gmail.com
* **Affiliation**: Department of Biosystems Engineering and Soil Science, The University of Tennessee, Knoxville, TN, USA

---

# 📜 License
MIT License.

---

# 🤝 Contributing
Contributions are welcome!

