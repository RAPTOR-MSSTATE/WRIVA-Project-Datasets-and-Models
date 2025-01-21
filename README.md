# WRIVA-Project-Datasets-and-Models
****Datasets and Models used for Artifact Segmentation****

The folders in this repo include the individual models created to detect specific image artifacts. These artifacts include rain, soil, and finger-in-lense.

Google Drive link containing Datasets, Models, and Annotations: https://drive.google.com/drive/folders/1_Ly1mvAFTeg6gQ2fiQH5AyigZ8hG34Wz?usp=drive_link

The Google Drive link contains individual folders for the rain, soil, and finger-in-lense datasets. These folders have all the annotations and working models created for each dataset.

We solely created the datasets contained in the Google Drive link. The drive consists of data sets for images with artifacts, including rain, soil, and finger-in-lense. These datasets were then used to train models capable of identifying and segmenting the specific artifact that each dataset was created around. Before training the model we annotated and labeled the artifacts in each of the images contained in the dataset and converted those annotations into a COCO-JSON file using an annotation software by makesense.ai. Each model was trained using Detectron2 for instance segmentation using our custom data.

**EXAMPLE OUTPUTS OF EACH MODEL**

###Rain Drop Example

![siteA01-camA051-2023-04-15-14-41-58-000011 (1)](https://github.com/user-attachments/assets/705ba95c-dc16-41de-a3e0-905c99ac0ec5)
Original

![EXAMPLE RAIN SITE A01](https://github.com/user-attachments/assets/ebde985a-84d7-4ea1-bc16-c9f6a4ceed8f)
Segmentation

###Soil Example


**Sources**

Detectron2 (Used to train each model): https://colab.research.google.com/github/bnsreenu/python_for_microscopists/blob/master/330_Detectron2_Instance_3D_EM_Platelet.ipynb#scrollTo=10QrSe6tbogs

MakesenseAI (Used to create the annotations for each dataset): https://www.makesense.ai/
