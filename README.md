# Labelme2YOLO

Convert LabelMe Annotation Tool JSON format to YOLO text file format.

## Parameters Explain
**--json_dir** LabelMe JSON files folder path.

**--val_size (Optional)** Validation dataset size, for example 0.2 means 20% for validation and 80% for training.

**--json_name (Optional)** Convert single LabelMe JSON file.

## How to Use

### Convert JSON Files, split training and validation dataset by --val_size
Put all LabelMe JSON files in to **labelme_json_dir**, and run this python command.
```bash
python labelme2yolo.py --json_dir /home/username/labelme_json_dir/ --val_size 0.2
```
Script would generate YOLO format dataset labels and images under different folders, for example,
```bash
/home/username/labelme_json_dir/YOLODataset/labels/train/
/home/username/labelme_json_dir/YOLODataset/labels/val/
/home/username/labelme_json_dir/YOLODataset/images/train/
/home/username/labelme_json_dir/YOLODataset/images/val/
```

### Convert JSON Files, split training and validation dataset by folder
If you already split train dataset and validation dataset for LabelMe by yourself, please put these folder under labelme_json_dir, for example,
```bash
/home/username/labelme_json_dir/train/
/home/username/labelme_json_dir/val/
```
Put all LabelMe JSON files in to **labelme_json_dir**. 
Script would read train and validation dataset by folder.
Run this python command.
```bash
python labelme2yolo.py --json_dir /home/username/labelme_json_dir/
```
Script would generate YOLO format dataset labels and images under different folders, for example,
```bash
/home/username/labelme_json_dir/YOLODataset/labels/train/
/home/username/labelme_json_dir/YOLODataset/labels/val/
/home/username/labelme_json_dir/YOLODataset/images/train/
/home/username/labelme_json_dir/YOLODataset/images/val/
```
