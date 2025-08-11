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



![lameness](https://github.com/user-attachments/assets/cec93c8d-b665-4f7d-9493-9d73d491691c)

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


# Citation
If you use this dataset, please cite:

```
Nasiri, A., Yoder, J., Zhao, Y., Hawkins, S., Prado, M. and Gan, H., 2022. Pose estimation-based lameness recognition in broiler using CNN-LSTM network. Computers and Electronics in Agriculture, 197, p.106931.
DOI: https://doi.org/10.1016/j.compag.2022.106931
```


```

# Installation
**Prerequisites**
    
* Python 3.6+
* Required Python packages:
```  
pip install opencv-python tkinter
```
**Setup**

**1.** Clone this repository:
```  
git clone https://github.com/AminNasiri63/YOLO-Image-Annotation-Tool.git
```
**2.** Navigate to the repository directory:
```  
cd YOLO-Image-Annotation-Tool
```
**3.** Install dependencies:
```  
pip install opencv-python
```
Note: tkinter usually comes pre-installed with Python, but if not, you may need to install it separately.

# Usage

**1.** Run the main script:
```  
python main.py
```
**2.** When prompted, select the folder containing the images you want to annotate.

**3.** The tool will open and display the first image in the folder.

**Controls:**

- **Left Mouse Button**: Draw a bounding box.
- **Right Mouse Button**: Delete a selected bounding box.
- **Middle Mouse Button**: Define class for the currently selected box.
- **S**: Save current annotations.
- **N**: Skip image without saving.
- **F**: Select new folder.
- **Q**: Quit tool.

# File Format
Annotations are saved in YOLO format text files with the same name as their corresponding image file but with a ```.txt``` extension. Each line in the text file represents one bounding box in the format:
```  
<class_id> <x_center> <y_center> <width> <height>
```
where:
- ```class_id```: Integer representing the class ID (0-indexed).
- ```x_center```, ```y_center```: Normalized coordinates (0-1) of the center of the bounding box.
- ```width```, ```height```: Normalized width and height of the bounding box (0-1).

# Folder Structure
Your initial folder structure:
```
📁 Parent_Directory/
│
└── 📁 Selected_Image_Folder/
    ├── 📄 image1.jpg
    ├── 📄 image1.txt (if already annotated)
    ├── 📄 image2.png
    └── ...
```
After running the tool, the structure will be:
```
📁 Parent_Directory/
│
├── 📁 Selected_Image_Folder/
│   ├── 📄 image1.jpg
│   ├── 📄 image1.txt (if already annotated)
│   ├── 📄 image2.png
│   └── ...
│
└── 📁 Results/
    │
    └── 📁 Selected_Image_Folder_Name_Final/
        ├── 📄 image1.jpg
        ├── 📄 image1.txt
        ├── 📄 image2.jpg
        └── ...
```
The tool reads images from the Selected_Image_Folder and saves annotation files in the Results/Selected_Image_Folder_Name_Final directory.

# Limitations
- **Box Drawing Constraints**: It is impossible to start drawing a new bounding box inside an existing box. When attempting to click inside an existing box, the tool will select or interact with that box instead of starting a new one.

# License
MIT License.

# Contributing
Contributions are welcome! Please feel free to submit a Pull Request.
