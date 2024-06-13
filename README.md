Methodology: **SVM, KNN, ISOMAP for Dimensionality reduction, PIL Image, vit-xray-pneumonia-classification open-source model, Visualization using matplotlib, mplot3d libraries**

Tools Used: **Python, Jupyter Notebook** | Category: **Supervised Learning, Classification** | Year: **2023, 2024**

# Image Classification
Medical image recognition and classification is one of the most important problems in the image recognition area. Its goal is to classify medical images into different categories to help doctors in disease diagnosis or further research. Accurately identified decease patterns on earlier stages can save lives. In the past, doctors used their professional expertise to classify the medical images. This is a difficult, tedious, and time-consuming task. Also, such approach is prone to instability and human error. In the last decades medical image classification research has gained a lot of momentum and progressed significantly. In this project, I am comparing several classification techniques including traditional ML methods, such as SVM and KNN, and an open-source pre-trained Neural Network model.

### Data
There are 1,583 normal and 4,273 pneumonia x-ray images of different sizes in the dataset. 
The data is sourced from Mendeley Data (https://data.mendeley.com/datasets/rscbjbr9sj/2)[1].


### Objective
Find an appropriate classification model that classifies images with high accuracy and recall.

### Summarized Approach
I used traditional classification algorithms such as SVM and KNN to classify preprocessed images into 2 groups: normal and pneumonia. To improve processing time I attempted a dimensionality reduction technique ISOMAP suitable for image data. I then fit classification models to compressed and original data. In addition, I tested an open-source classification model from HuggingFace (https://huggingface.co/lxyuan/vit-xray-pneumonia-classification) on the same dataset. This model is a fine-tuned version of google/vit-base-patch16-224-in21k on the chest x-ray classification dataset.

### Results
![Untitled](https://github.com/aidatabaeva/image-classification/assets/121254366/8089fc9c-333b-4439-8039-2ea04351480f)

The selection of the model depends on the business priority. There is a model that saves processing time, one that maximizes accuracy, and one that maximizes recall. Given the nature of medical problems — where false positives are often more acceptable than false negatives because the diagnosis is usually followed by an additional exam — recall should be given higher priority.

In this context, the performance difference between the neural network (NN) model and the traditional model is not very significant. Therefore, a traditional SVM can be effectively used for this particular classification problem, ensuring high recall while maintaining overall accuracy.

**Business Priority:** The choice of model depends on what is prioritized — processing time, accuracy, or recall.
**Medical Context:** In medical diagnostics, false negatives (missed detections) can be more dangerous than false positives. Therefore, recall is crucial.
**Model Selection:** Although there might be a slight performance difference between a neural network and a traditional model, the traditional SVM is a suitable choice due to its balance of high recall and accuracy.

[1] Kermany, Daniel; Zhang, Kang; Goldbaum, Michael (2018), “Labeled Optical Coherence Tomography (OCT) and Chest X-Ray Images for Classification”, Mendeley Data, V2, doi: 10.17632/rscbjbr9sj.2
