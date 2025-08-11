# Broiler Lameness Pose Estimation Dataset
This dataset contains a large-scale benchmark of **240 broilers** with a total of **9,214 high-resolution** images (1280×720, PNG format).
It is designed for **broiler pose estimation** and **lameness detection tasks**, and includes manually annotated anatomical key points and a defined pose skeleton.
All annotations are stored in Comma-Separated Values (CSV) format.

The dataset was created to support research in:
* Animal welfare monitoring.
* Computer vision–based lameness assessment.
* Pose estimation and keypoint detection.


# Keypoint Definitions & Pose Skeleton
Each broiler image is annotated with 7 anatomical key points:

| Key Point ID | Name      | Description              |
| ------------ | --------- | ------------------------ |
| 1            | Center    | Center point of the body |
| 2            | Head      | Tip of the head          |
| 3            | Tail      | Tip of the tail          |
| 4            | RightKnee | Right knee joint         |
| 5            | RightHeel | Right heel joint         |
| 6            | LeftKnee  | Left knee joint          |
| 7            | LeftHeel  | Left heel joint          |


![lameness](https://github.com/user-attachments/assets/84c5b68a-53a8-4315-8e62-20cbb663f33a)



# Data Structure

```
📁 Lameness/
│
└── 📁 Broiler_ID/
    ├── 📄 img50.png
    ├── 📄 img52.png
    └── ...
    ├── 📄 CollectedData.csv

└── ...

└── 📁 Broiler_ID/
    ├── 📄 img15.png
    ├── 📄 img17.png
    └── ...
    ├── 📄 CollectedData.csv 
```
# Annotation Format
Each ```CollectedData.csv``` file has the following structure:

* **First row**: ```bodyparts``` -- lists all annotated key points (each with x and y columns).
* **Second row**: ```coords``` -- specifies the coordinate axes (x, y).
* **Subsequent rows**: One row per image, starting with the file name followed by coordinates for each key point.

**Example**:
```
bodyparts    Center  Center  Head  Head  Tail  Tail  LeftKnee  LeftKnee  LeftHeel  LeftHeel  RightKnee  RightKnee  RightHeel  RightHeel
coords       x       y       x     y     x     y     x         y         x         y         x          y          x          y
img50.png    695.27  156.31  659.05 88.39 745.72 171.18         ...      697.21 197.70  690.09 209.35    ...        ...        ...
img52.png    665.51  138.20  647.40 70.28 712.73 151.13         ...      688.15 190.59  688.80 208.70    ...        ...        ...
```
**Note**: Missing values indicate that the key point is not visible in the image.Data Summary

# Data Summary
| Attribute            | Value    |
| -------------------- | -------- |
| Number of broilers   | 240      |
| Total images         | 9,214    |
| Image resolution     | 1280×720 |
| Image format         | PNG      |
| Key points per image | 7        |
| Annotation format    | CSV      |


## 📦 dataset Download
You can directly download the dataset Download from:

# Citation
If you use this dataset, please cite:

```
Nasiri, A., Yoder, J., Zhao, Y., Hawkins, S., Prado, M. and Gan, H., 2022. Pose estimation-based lameness recognition in broiler using CNN-LSTM network. Computers and Electronics in Agriculture, 197, p.106931.
DOI: https://doi.org/10.1016/j.compag.2022.106931
```

# Contact
* **Name**: Hao Gan -- Amin Nasiri
* **Email**: hgan1@utk.edu -- aminnassiri63@gmail.com
* **Affiliation**: Department of Biosystems Engineering and Soil Science, The University of Tennessee, Knoxville, TN, USA

# 📜 License
MIT License.

# 🤝 Contributing
Contributions are welcome!
