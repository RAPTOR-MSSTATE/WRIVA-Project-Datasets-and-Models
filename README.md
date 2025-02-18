# WRIVA-Project-Datasets-and-Models
****Datasets and Models used for Artifact Segmentation****

The folders in this repo include the individual models created to detect specific image artifacts, such as rain, soil, and finger-in-lense.

Google Drive link containing Datasets, Models, and Annotations: https://drive.google.com/drive/folders/1_Ly1mvAFTeg6gQ2fiQH5AyigZ8hG34Wz?usp=drive_link

The Google Drive link contains individual folders for the rain, soil, and finger-in-lense datasets. These folders have all the annotations and working models created for each dataset.

We solely created the datasets contained in the Google Drive link. The drive consists of data sets for images with artifacts, including rain, soil, and finger-in-lense. These datasets were then used to train models capable of identifying and segmenting the specific artifact that each dataset was created around. Before training the model, we annotated and labeled the artifacts in each of the images contained in the dataset and converted those annotations into a COCO-JSON file using an annotation software by makesense.ai. Each model was trained using Detectron2 for instance segmentation using our custom data.

### Rain Drop Pre-training Annotation Example

<img width="471" alt="IMG_1748 2" src="https://github.com/user-attachments/assets/620e30ee-27a6-4353-beba-c86a49c37484" />
<img width="471" alt="Screenshot 2025-02-18 at 8 23 10 AM" src="https://github.com/user-attachments/assets/bc9bbfa0-c098-487e-a734-50fc04c6c1c3" />

### Soil Pre-training Annotation Example

<img width="471" alt="IMG 2161" src="https://github.com/user-attachments/assets/773a62a2-ab74-4bb4-9989-6bb348616201" />
<img width="471" alt="Screenshot 2025-02-18 at 8 50 43 AM" src="https://github.com/user-attachments/assets/530ef844-6b11-4d80-8d13-75a9169f0c0f" />

### Finger in Lense Pre-training Annotation Example

<img width="471" alt="Image28-obstruction" src="https://github.com/user-attachments/assets/4964395a-b9ac-4299-97fe-d9e75ee3862d" />
<img width="471" alt="Screenshot 2025-02-18 at 8 58 58 AM" src="https://github.com/user-attachments/assets/03e00e9c-9806-4f80-a628-4dfbd60bb2f8" />


### Colab File Used to Train Our Models
https://colab.research.google.com/drive/1-59uZ6JBe-3zA5GJITm2ZWocBQmKRJZs?authuser=1#scrollTo=2z8JER1KM2Ul

## Train Your Own Model Using Detectron2

This guide provides step-by-step instructions to train a custom **instance segmentation model** using **Detectron2** using the **provided Google Colab File above**. It covers dataset preparation, model training, and evaluation.

---

## **1. Prepare Your Dataset**
- Annotate images using an annotation tool like [MakeSense.ai](https://www.makesense.ai/).
- Export annotations in **COCO JSON format**.
- Ensure that images and annotation files are organized properly in your Google Drive for easy access. There should be a training folder containing your training images and COCO JSON file and a validation folder containing your validation images and COCO JSON file. **Use the Google Drive link at the beginning of the README for an example of how to set up your files.**

---

## **2. Set Up Your Environment**
- Follow the given code to install **Detectron2** and its dependencies in Google Colab.

---

## **3. Configure Your Dataset**
- Run blocks of code to define paths to **training** and **validation** datasets. You will use the folders that were created in step one to define the training and validation paths.

---

## **4. Visualize Sample Annotations**
- Load and display a few annotated images to verify correctness.
- Ensure that objects are properly labeled and segmented.

---

## **5. Configure the Model**
- Set hyperparameters such as:
  - **Batch size**
  - **Learning rate**
  - **Number of iterations**
  - **Number of object classes**
- Make sure the number you set for your object classes matches the number of unique artifact classes that were annotated.
- Define an output directory to save model checkpoints.

---

## **6. Train the Model**
- Start training using `DefaultTrainer()`.
- Training may take an extended time to complete.
- Save the trained model weights once training is complete.

---

## **7. Perform Segmentation on New Images**
- Load the trained model.
- Set a confidence threshold for predictions.
- Test on validation images to visualize segmentation results.

---

## **9. Process Multiple Images**
- Run the model on all images in a folder.
- Save segmented output images to an output directory.

---

**Sources**

Detectron2 (Used to train each model and create our own tailored custom training script): https://colab.research.google.com/github/bnsreenu/python_for_microscopists/blob/master/330_Detectron2_Instance_3D_EM_Platelet.ipynb#scrollTo=10QrSe6tbogs

MakesenseAI (Used to create the annotations in COCO JSON format for each dataset): https://www.makesense.ai/
