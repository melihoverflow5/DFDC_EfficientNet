# **Deepfake Detection Model**

## **Overview**

This project focuses on detecting **deepfakes** by training a model on a dataset of real and manipulated (fake) images. The model is built using **EfficientNetB3** as a pre-trained backbone, fine-tuned to classify images as either **real** or **fake**. The project is implemented entirely in a **Google Colab** notebook, making it easy to replicate the results without any local setup required.

## **Project Structure**

The entire project is contained within a **Google Colab notebook** where the following tasks are performed:
1. **Data Preprocessing**
2. **Model Definition**
3. **Training**
4. **Evaluation**

All code can be executed directly within the Colab notebook.

## **Requirements**

Since the entire project is implemented within a **Google Colab notebook**, all the necessary dependencies are pre-installed. If you plan to run this locally, you can install the following dependencies:

```bash
pip install tensorflow matplotlib scikit-learn seaborn numpy
```

## **Dataset**

The model is trained on the **dfdc_part_34** from **Kaggle** which consist cropped face images into **150x150** from part of **Deepfake Detection Challenge Dataset**.

### **Dataset Details**:
- **Source**: [dfdc_part_34 (Kaggle)](https://www.kaggle.com/datasets/greatgamedota/dfdc-part-34)
- **Size**: The dataset contains approximately **27,000 images** (divided into training, validation, and test sets).
- **Classes**:
  - **REAL**: Images that are authentic and not manipulated.
  - **FAKE**: Images that have been manipulated using deepfake technology.
- **Preprocessing**:
  - Images are resized to **150x150 pixels**.
  - Pixel values are normalized to the range **[0, 1]**.
  - The dataset is split into **training**, **validation**, and **test** sets based on the metadata.

### **Dataset Split**:
- **Training Set**: Contains a majority of the dataset used to train the model.
- **Validation Set**: Used during training to evaluate the model's performance on unseen data and prevent overfitting.
- **Test Set**: Used to evaluate the final performance of the model after training.

### **Accessing the Dataset**:
To use this dataset with Google Colab, download it from Kaggle then upload to Google Drive.


## **Conclusion**

In this project, a deep learning model for deepfake detection was developed using EfficientNetB3 as the backbone network. The model was fine-tuned on a dataset of real and fake images to classify them effectively. The results demonstrate strong performance, with an AUC-ROC of **0.9315**, an accuracy of **92.1%**, and an F1 Score of **95.46%**, indicating that the model is capable of distinguishing between real and manipulated images with high precision.

The project utilized mixed precision training to speed up computation and reduce memory usage, allowing the model to train efficiently on the available hardware. The training process was monitored using TensorBoard, which provided insightful metrics, and the best model was saved and made available for download.
