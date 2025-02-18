# WRIVA-Project-Datasets-and-Models
****Datasets and Models used for Artifact Segmentation****

The folders in this repo include the individual models created to detect specific image artifacts. These artifacts include rain, soil, and finger-in-lense.

Google Drive link containing Datasets, Models, and Annotations: https://drive.google.com/drive/folders/1_Ly1mvAFTeg6gQ2fiQH5AyigZ8hG34Wz?usp=drive_link

The Google Drive link contains individual folders for the rain, soil, and finger-in-lense datasets. These folders have all the annotations and working models created for each dataset.

We solely created the datasets contained in the Google Drive link. The drive consists of data sets for images with artifacts, including rain, soil, and finger-in-lense. These datasets were then used to train models capable of identifying and segmenting the specific artifact that each dataset was created around. Before training the model we annotated and labeled the artifacts in each of the images contained in the dataset and converted those annotations into a COCO-JSON file using an annotation software by makesense.ai. Each model was trained using Detectron2 for instance segmentation using our custom data.

### Rain Drop Example

![IMG_1748 2](https://github.com/user-attachments/assets/620e30ee-27a6-4353-beba-c86a49c37484)
<img width="471" alt="IMG_1748 2" src="https://github.com/user-attachments/assets/620e30ee-27a6-4353-beba-c86a49c37484" />
Original

<img width="471" alt="Screenshot 2025-02-18 at 8 23 10 AM" src="https://github.com/user-attachments/assets/bc9bbfa0-c098-487e-a734-50fc04c6c1c3" />
Segmentation

### Soil Example
[EXAMPLE SOIL 77.pdf](https://github.com/user-attachments/files/18494828/EXAMPLE.SOIL.77.pdf)


**Sources**

Detectron2 (Used to train each model): https://colab.research.google.com/github/bnsreenu/python_for_microscopists/blob/master/330_Detectron2_Instance_3D_EM_Platelet.ipynb#scrollTo=10QrSe6tbogs

MakesenseAI (Used to create the annotations for each dataset): https://www.makesense.ai/
