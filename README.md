# 🛠️ AI-Powered Quality Control for Casting Products
#### This projekt demonstrates the classification of industrial casting parts using Deep Learning. The primary goal is to automate the quality assurance process by distinguishing between **defect-free parts(OK)** and **defective parts (DEFECT)**.

## 🚀 Project Overview
#### The project evaluates three diffrenet model architectures. The final implementation using '' archieved an accuracy of ''.

### Model Performance Comparison
| Model | Accuracy | Test Loss | Characteristics |
| :--- | :--- | :--- |:--- |
|**Baseline** | ~ |~  | Two linear layers with ReLU activation|
|**Custom CNN** | ~ |~  | Convolutional Neural Network optimized for 1-channel grayscale images|
|**ResNet18 (Transfer Learning)** | ~ |~  | Top-performing model utilizing pre-trained ImageNet weights|

## 🏗️ Model Architectures
### 1. Baseline Model
#### A basic feed-forward Multi-Layer Perceptron (MLP) used to establish a performance floor:
* **Two Linear Layers:** Mapping flattend pixel data to class probabilities.
*  **ReLU Activation:** Introduced between layers to handle non-linear relationships.
*   **Input:** Flattened 224x224 grayscale images.

### 2. Custom CNN
#### A deeper architecture designed to capture spatial features through:
* **Convolutional Layers:** For automatic feature extraction (edges, textures).
* **Max Pooling:** To reduce dimensionality and increase computation efficiency.

### 3. ResNet18
#### A Residual Network (ResNet18) adapted for this specific task:
* **Modified Input Layer:** Adjustied to accept 1-channel grayscale images (instead of 3-channel RGB).
* **Transfer Learning:** Fine-tuned from ImageNet pre-trained weights to leverage complex feature recognition.


## 📂Dataset Details
#### The modelwas trained and tested on a dataset of 1-channel grayscale images. The dataset is well-balanced, which is crucial for reliable classification results.

* **Total Dataset:** 7348 images.
    * **Defective (def_front):** 3758 images:
    *  **OK(ok_front):** 3590 images.
* **Data Split:** The data was divided into Training (approx. 90%) and Testing(approx. 10%) sets.

### Dataset Visualization
#### The following chart visualizes the distribution of the two classes ('def_front' and 'ok_front') across the training and testing splits. The balance between classes prevent model bias towards one category.

![Dataset Distribution](data_distribution.png)

* **Original Resolution:** The images were originally **512x512** pixels.
* **Processed Resolution:** Resized to **224x224** pixels for optimal model performance.
* **Preprocessing:** Grayscale normalization and strategic padding to maintain structural edge details during convolution.


## 📊 Evaluation & Insights
#### A **Confusion Matrix** was generated to analyse the reliability of the classification across all three models.  !!!!! noch machen 

![Confusion Matrix Comparison](confusion_matrix_final.png)

## 🛠️ Technical Stack
* **Language:** Python
* **Framework:** Pytorch, Torchvision
* **Data Processing:** Scikit_learn, Matplotlib, NumPy
* **Environment:** Google Colab /Jupyter Notebook


## Summary
The transition from a linear baseline to a Transfer Learning approach with ResNet18 resulted in a significant performance increase. **!!!! weitermachen** 




