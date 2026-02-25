ResCD-CSI: Residential Construction Image Dataset Using CSI Divisions for Deep Learning-based Object Detection
===========================================

Version: 1.0
Author: SARBEL Lab
License: CC BY 4.0

-------------------------------------------
Overview
-------------------------------------------
The Construction Scene Object Detection Dataset contains labeled images from active construction environments, representing materials, elements, and activities observed across multiple project stages. 
It supports computer vision research focused on automated construction monitoring, activity detection, and progress tracking.

This dataset is annotated in YOLO format and designed for use with state-of-the-art object detection frameworks such as YOLOv9–YOLOv11.

-------------------------------------------
Folder Structure
-------------------------------------------
root/
│
├── Dataset_Repository/
│   ├── Class-1/
│   ├── Class-2/
│   └── ..../
├── Metadata/
│   ├── dataset_description.json
│   ├── image_properties.json
│   ├── construction_stages.json
├── YOLO_split.zip
├── data.yaml
└── README.txt

Each annotation file uses YOLO format:
<class_id> <x_center> <y_center> <width> <height>
All coordinates are normalized (0–1 range).

-------------------------------------------
Classes
-------------------------------------------
The dataset includes 40 object categories representing major construction materials, activities, and elements organized according to major CSI division.  
The full class list is provided in data.yaml.

-------------------------------------------
Getting Started
-------------------------------------------
Download the github and dataset repository:
Dataset: http://dx.doi.org/10.6084/m9.figshare.30325087
git clone [https://github.com/sarbel-org/ResCD-CSI]

In the main folder, you will find YOLO_split.zip, a ready-made classified dataset with 75/15/15 split for train, val, and test. If you want to use this, move to Step 2.

Step 1: Custom Split / Classes
If you want a custom split or have custom classes, follow these instructions:
01_Classes_Folder_Name.ipynb: Renumber classes if any folders are removed or renamed.
02_Annotation_Renumbering.ipynb: Update annotation numbering in .txt files if you add/remove classes.
03_Yolo_Classification.ipynb: Split the dataset in a custom ratio (e.g., 70/15/15). Running this creates the YOLO_split folder.
Add data.yaml to the YOLO_split folder and update class names if needed. Zip the folder again if necessary.

Step 2: Google Drive / Colab
Upload to Google Drive:
Create YOLO_Project folder and upload YOLO_split.zip and notebook 04 to this folder. Run the notebook in Google Colab:
Open 04_Construction_Image_Dataset_Yolo11_V1_0.ipynb
Use T4 GPU runtime for faster training
Follow the notebook instructions to load data and run the model.

Auxiliary Scripts: Scripts are included to rename all images and annotations if needed for consistency.

-------------------------------------------
Construction Stage Classification
-------------------------------------------
Using the meta/construction_stages.json you can also classify the output of the object detection into a different construction stages for progress monitoring

-------------------------------------------
Utility Scripts
-------------------------------------------
10_Renaming_Files - use to rename all the files based on their parent folder
11_Object_Count - Counts and summarizes the number of annotations per class.

-------------------------------------------
Metadata
-------------------------------------------
Stored in /meta/:
- dataset_description.json — provides a description of the dataset
- image_properties.json — number of images, size etc.
- construction_stages.json — mapping of classes to project stages

-------------------------------------------
Dataset Applications
-------------------------------------------
- Construction activity and progress detection
- Material and element recognition
- Temporal analysis of project stages
- Automated visual inspection research

-------------------------------------------
Citation
-------------------------------------------
If you use this dataset, please cite:

Iqbal and Mirzabeigi, ResCD-CSI: Residential Construction Image Dataset Using CSI Divisions for Deep Learning-based Object Detection, 2025.
Available at: http://dx.doi.org/10.6084/m9.figshare.30325087

-------------------------------------------
Future Updates
-------------------------------------------
- Semantic and instance segmentation annotations
- Additional multi-view image sets
- Integration of temporal data for progress tracking

-------------------------------------------
Contact
-------------------------------------------
For questions or collaborations:
Dr. Shayan Mirzabeigi
Email: smirzabeigi@esf.edu (please ref. to website for latest info)
Website: https://sarbel.org
Github: https://github.com/sarbel-org/

© 2026 SARBEL — Released under Creative Commons Attribution 4.0 License.



