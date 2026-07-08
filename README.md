# Breast-Cancer-Detection-Using-Yolov9-Model
leveraging YOLOv9, a state-of-the-art deep learning object detection model, to automate the detection and classification of breast lesions in ultrasound images. 
## Overview
Breast cancer is one of the leading causes of cancer-related deaths among women worldwide, where early detection is critical for improving survival rates. Although breast ultrasound is a safe, cost-effective, and widely used imaging modality, its interpretation is often challenging due to image complexity and reliance on expert radiologists.

This project leverages YOLOv9, a state-of-the-art deep learning object detection model, to automate the detection and classification of breast lesions in ultrasound images. By applying computer vision and artificial intelligence, the model aims to accurately identify benign, malignant, and normal breast tissues, supporting faster and more reliable diagnosis.

The goal of this research is to enhance early breast cancer detection, reduce operator dependency, and contribute to improved clinical decision-making through AI-assisted medical image analysis.
## Objectives
- Acquire data images from the National Institute of Cancer (NIC, Brazil) to fine-tune a YOLO deep-learning model for breast cancer detection.
- Pre-processing of the images in our dataset to adapt them to the Deep Learning model.
- Finetune the YOLO Deep Learning (DL) model to detect and distinguish malignant
from benign breast tumors.
- Evaluate the model’s performance in detecting malignant or benign breast ultrasound
images.
# Methodology
## Workfow
1. Data Acquisition
2. Data Preprocessing
3. Data Preparation
4. Transfer Learning
5. Model Training
6. Performance Evaluation
7. Results
## Development Tools
- jupiter Notebook
- Python
- Pytorch
- Opencv
- Numpy
- Pandas
- Matploitlib
# Dataset
## Ultrasound Dataset 
The dataset used is BUS- BRA (Breast Ultrasound Dataset), obtained from the National Institute of Cancer (NCI), Brazil. It was specifically developed to support the development and validation of computer-aided diagnosis (CAD) systems for breast ultrasound, providing a standardized benchmark for AI research in breast lesion detection, segmentation, and classification. The dataset contains a total of 1,875 grayscale PNG images collected from 1,064 female patients aged between 16 and 89 years [15]. Each image has a resolution of 224 × 224 pixels, and corresponding segmentation masks were manually annotated by an expert ultra sonographer to ensure reliability.
# Data Preprocessing Technigues
The following preprocessing and transforms techniques were used.
## Image Preprocessing
- Image Resize
- Normalization
- Benign Downsampling
## Transforms
- Rotations
- Flips
- Brightness adjustments
- Noise injection
### These Techniques were applied to:
- Ensure uniformity across the dataset
- Reduce variations caused by different ultrasound machines and imaging conditions
- To further make sure all images are in a format and style that the model can understand.
- Prevent overfitting of the model.
## YOLOv9 Model
Yolov9 is real time object detection model that builds upon improvements made in previous versions. It leverages advanced techniques like Generalized Efficient Layer Aggregation Network (GELAN) and Programmable Gradient Information (PGI) to deliver superior performance across the board.
## Model Architecture
This project adapts the YOLOv9 architecture for breast ultrasound image analysis through task-specific modifications to improve detection accuracy, efficiency, and interpretability.

- The GELAN backbone was made lighter by reducing network depth to minimize overfitting on the relatively small ultrasound dataset. Attention mechanisms (Squeeze-and-Excitation and channel-spatial attention) were integrated to enhance lesion features while suppressing background noise.
- A simplified multi-scale feature fusion network was implemented with reduced depth and channel dimensions. Spatial Pyramid Pooling (SPP) and an additional feature refinement stage were incorporated to improve contextual feature extraction and robustness to low-contrast ultrasound images.
- The detection head was decoupled into separate branches for bounding box regression, classification, and objectness prediction. Bounding box localization was simplified using direct coordinate prediction, reducing computational complexity and improving interpretability. The classification head was customized for binary classification of benign and malignant breast lesions.
These architectural modifications enable the model to better capture subtle lesion characteristics while maintaining computational efficiency for automated breast cancer detection in ultrasound images.
# Results
## DETECTION RESULTS ON THE DATASET
|Classes |	P (%)	| R (%)|	mAP@0.5 (%)|
|:-------|:-------|:-----|:------------|
|All |	82.1 |	87.7	| 91.1 |
|Benign	| 80.7 |	91.9 |	90.7 |
|Malignant |	83.5 |	83.5	| 91.6 |

## Visualization
The results provided visuals which include:
- Confusion Metrix of model
- Recall Confidence Curve
- Precision Confidence Curve.
# Application
Potential APllications of this work include:
- Computer-Aided Diagnosis for rdiologist
- Breast Cancer screening in resource-limited settings
- Medical Education and research
  # Author
Gloria Otemah Biomedical Engineering Graduate University of Ghana, Legon Gmail: gloriaotemah334@gmail.com

Clara Otipeseku Amakuor Biomedical Engineering Graduate University of Ghana, Legon Gmail: claraotipeseku3@gmail.com

Emmanuella Selassie Nartey Biomedical Engineering Graduate University of Ghana, Legon Gmail: narteyemmanuella77@gmail.com

Vanessa Naa-Atswei Adjei Biomedical Engineering Graduate University of Ghana, Legon Gmail: adjeivanessa45@gmail.com
# Reference
1. World Health Organization (WHO).” Https://www.who.int/news-room/fact-sheets/detail/breast-Cancer. Breast Cancer. WHO Fact Sheets, March 26, 2023.
2. Iacob, R., Iacob, E. R., & colleagues. (2024). Evaluating the role of breast ultrasound in early detection of breast cancer in low- and middle-income countries: A comprehensive narrative review. Journal/Publisher.
3. Gomez-Flores, Wilfrido, Maria Julia Gregorio-Calas, and Wagner Coelho de Albuquerque Pereira. “BUS-BRA: A Breast Ultrasound Dataset for Assessing Computer-Aided Diagnosis Systems.” American Association of Physicists in Medicine 51, no. 4 (2023). https://doi.org/10.1002/mp.16812.
# Lincense
This project is released under the MIT License.





