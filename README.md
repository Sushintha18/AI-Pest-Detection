# AI-Pest-Detection
## AI Pest Detection Using YOLOv8
### Project Overview

This project focuses on detecting crop diseases and pests using a deep learning object detection model. The system uses the YOLOv8 model to identify different crop diseases from images and helps in early detection for better agricultural management.

The model is trained on a dataset obtained from Roboflow and implemented using Python in Google Colab.

### Technologies Used

- Python
- YOLOv8 (Ultralytics)
- Roboflow Dataset
- OpenCV
- PyTorch
- Google Colab
- Dataset

The dataset was obtained from Roboflow and exported in YOLOv8 format.
It contains labeled images of crop diseases used to train and validate the model.

### Dataset features:

- Annotated crop disease images
- Training and validation data
- YOLO format labels
- Installation

### Install required libraries:

bash 
```
pip install ultralytics
pip install
``` 


### Dataset Download:
bash
```
from roboflow import Roboflow

rf = Roboflow(api_key="lL56ENgbETMdUDoZ6lw2")
project = rf.workspace("sushinthas-workspace").project("crop-disease-srixo-0iros")
version = project.version(1)
dataset = version.download("yolov8")
```
### Model Training

The YOLOv8 model is trained using the following configuration:

bash
```
from ultralytics import YOLO
model = YOLO("yolov8n.pt")
model.train(
    data="/content/crop-disease-1/data.yaml",
    epochs=50,
    imgsz=640
)
```

### Training parameters:

Model: YOLOv8 Nano
Epochs: 50
Image Size: 640

### Model Architecture

The YOLOv8 model contains multiple convolutional layers used for feature extraction and object detection. The trained model detects multiple crop diseases with bounding boxes and confidence scores.

### Output

The trained model can detect crop diseases in images and highlight them with bounding boxes.

Example output:



### Applications

- Smart agriculture systems
- Automated crop monitoring
- Early disease detection in plants
- AI-powered farming solutions

### Future Improvements

- Real-time pest detection using camera input
- Integration with mobile applications
- Higher accuracy with larger datasets
- Deployment on edge devices
