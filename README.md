# Custom-Image-Classification

## **Google Colab Link:** https://colab.research.google.com/drive/1Hu1OM8OA4_WFLJhSYfXmFg12FiKzGMdf?usp=sharing

## **ACTIVITY 3**

## **Guide Questions (Student Reflection & Explanation)**

## **1. Dataset Preparation**

- **How did you organize your dataset in Google Drive?**

I organized my dataset in Google Drive by creating a main project folder and separating the images into subfolders based on their class labels (plant species).

- **Why is folder structure important for TensorFlow image loading?**

A proper folder structure is important for TensorFlow image loading because it lets the framework automatically assign labels based on subfolder names. Each subfolder represents a class, which ensures images are correctly labeled, reduces misclassification, and allows functions like image_dataset_from_directory() to load data efficiently. It also makes adding new classes easier and helps keep the dataset organized for debugging and training.

## **2. Model Training**

- **What is the role of convolutional layers in image classification?**

Convolutional layers extract important features from images, such as edges, shapes, and patterns, allowing the model to recognize and classify objects accurately.

- **Why do we split data into training and validation sets?**

I split data into training and validation sets to train the model on one set of data (training set) and evaluate its performance on unseen data (validation set). This helps check if the model is learning patterns correctly without overfitting, ensures it can generalize to new images, and guides adjustments to improve accuracy.

## **3. Performance Analysis**

- **What accuracy did your model achieve?**

My model achieved an accuracy, which reflects how well it correctly classified the images in the validation set. This indicates the model’s ability to recognize and distinguish between the different plant species in the dataset.

- **How did the number of images affect the model’s performance?**

The number of images per class directly affected the model’s performance. Classes with more images generally allowed the model to learn better features, resulting in higher accuracy, while classes with fewer images were more prone to misclassification because the model had less data to recognize patterns. In general, having a balanced and sufficient number of images for each class improves overall model reliability and reduces bias.

## **4. Critical Thinking**

- **What challenges did you encounter while using your own dataset?**

While using my own dataset, I encountered several challenges. Collecting enough high-quality images for each class was time-consuming, and some images were blurry, poorly lit, or duplicated, which could reduce model accuracy. Ensuring that each class had a balanced number of images was also difficult, leading to potential bias in training.

- **How can data augmentation improve your model?**

Data augmentation can improve a model by artificially increasing the size and diversity of the dataset. Techniques like rotation, flipping, zooming, and brightness changes help the model learn to recognize objects under different conditions, reduce overfitting, and improve its ability to generalize to new, unseen images, resulting in higher accuracy and more robust performance.

## **5. Application**

- **Suggest a real-world application for your trained model.**

A real-world application for my trained model is in plant identification for agriculture or herbal research. Farmers or gardeners could use a smartphone app to quickly identify plant species by taking a photo, helping with crop management, pest control, or herbal medicine studies. It could also be used in educational tools to teach students about different plants and their properties.

- **How can this system be integrated into a mobile or web application?**

This system can be integrated into a mobile or web application by exporting the trained model (for example, from Teachable Machine) and embedding it into the app. For a mobile app, frameworks like TensorFlow Lite allow the model to run directly on smartphones, enabling users to take a photo and get instant plant classification. For a web application, the model can be hosted online and connected via JavaScript or a backend server, letting users upload images through a browser and receive real-time predictions. This integration makes the system accessible, interactive, and practical for everyday use.

## **ACTIVITY 3A**

## **Guide Questions (Student Explanation & Reflection)**

### **Visualization & Overfitting**

**1. What signs indicated overfitting in your first model?**

Signs of overfitting in my first model included very high training accuracy but much lower validation accuracy, along with validation loss increasing while training loss continued to decrease. This indicated that the model was memorizing the training images instead of learning patterns that generalize to new data.

**2. How did data augmentation affect validation accuracy?**

Data augmentation improved validation accuracy by increasing the diversity of the training images, such as through rotations, flips, and zooms. This helped the model generalize better to unseen images, reducing overfitting and making the predictions on the validation set more reliable.

### **Model Improvement**

**3. What is the purpose of dropout layers?**

The purpose of dropout layers is to prevent overfitting by randomly “dropping out” a fraction of neurons during training. This forces the model to learn redundant and robust features instead of relying too heavily on specific neurons, improving its ability to generalize to new data.
   
**4. Why does data augmentation improve generalization?**

Data augmentation improves generalization by artificially increasing the variety of training images through transformations like rotation, flipping, and zooming. This exposes the model to different scenarios and variations of the same class, helping it recognize patterns in unseen data and perform better on real-world images.

### **Performance Comparison**

**5. Compare accuracy before and after improvements.**

Before improvements, the model had lower validation accuracy due to overfitting and limited training data. After applying techniques like data augmentation and dropout layers, the accuracy significantly increased, showing better generalization to unseen images.

**6. Which technique contributed most to improvement?**

The technique that contributed most to improvement was data augmentation, as it expanded the variety of training images, allowing the model to learn more robust features and reduce overfitting.

### **Deployment & Application**

**7. Why is saving the model important?**

Saving the model is important because it allows you to reuse the trained model without retraining, share it with others, and deploy it in applications like mobile apps or web systems, saving time and computing resources.
  
**8. How can this model be deployed in a real-world system?**

This model can be deployed in a real-world system by exporting it (e.g., TensorFlow Lite for mobile or a web-compatible format for browsers) and integrating it into an app or website. Users can then upload or capture images, and the system will provide instant plant classification, making it practical for agriculture, herbal research, or educational tools.
