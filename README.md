---
license: mit
language:
- en
base_model:
- Ultralytics/YOLO11
pipeline_tag: object-detection
---
# YOLO-11N: Object Detection Model Trained on Objects365

## Overview

YOLO-11N is a custom object detection model based on the YOLO architecture, trained using the Objects365 dataset. This model is optimized for detecting a diverse range of objects in natural environments, leveraging the large-scale and high-quality annotations of Objects365.

## Training Dataset: Objects365

The Objects365 dataset is a comprehensive dataset designed for object detection tasks, containing:

- **365 object categories**
- **2 million high-resolution images**
- **30+ million annotated bounding boxes**

Objects365 provides a rich and complex benchmark for object detection models, ensuring robust generalization across various scenarios. The dataset is widely used for training deep learning models, offering detailed bounding box annotations for improved detection accuracy.

## Model Details

- **Model Architecture:** YOLO-11N (custom YOLO version optimized for Objects365)
- **Backbone:** Custom feature extractor
- **Training Dataset:** Objects365
- **Number of Classes:** 365
- **Input Image Size:** Configurable (default: 640x640)
- **Training Framework:** PyTorch (Ultralytics YOLO)
- **Preprocessing:** Standard YOLO preprocessing, including image resizing and augmentation

## Performance

The YOLO-11N model demonstrates high accuracy on the Objects365 validation set, benefiting from the extensive and diverse annotations provided by the dataset. The model is suitable for real-time object detection applications across various domains.

## Usage

To use the model for inference:

```python
from ultralytics import YOLO

# Load the model
model = YOLO('yolo11n_object365.pt')

# Run inference on an image
results = model('image.jpg')

# Display results
results.show()
```

## Applications

- Autonomous systems (drones, robotics)
- Surveillance and security
- Retail and inventory management
- Smart cities and traffic analysis
- General object detection research

## Acknowledgments

This model was trained using the **Objects365 dataset**, developed by Megvii. Special thanks to the open-source community for continuous improvements in object detection architectures.

For more details, visit the [Objects365 dataset page](https://docs.ultralytics.com/ru/datasets/detect/objects365/) and the [Ultralytics YOLO documentation](https://docs.ultralytics.com/).
