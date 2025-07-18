# 🇵🇰 Pakistani\_Celebrities\_Gender\_And\_Name\_Classification

This project focuses on detecting, classifying, and identifying Pakistani celebrities by leveraging deep learning techniques. It uses YOLOv8 for **face detection and gender classification**, and Keras ResNet50 for **name (identity) recognition** based on cropped facial features.

---

## 🔍 Project Overview

* **YOLOv8m** is trained for:

  * Detecting **faces** of Pakistani celebrities in images/videos.
  * Classifying detected faces by **gender** (male/female).
* **Keras ResNet50** is trained on:

  * The **cropped face images** extracted via YOLO.
  * Recognizing and classifying the **name (identity)** of the celebrity.

---

## 📁 Dataset Structure

The dataset should consists of:

* **15 known any Pakistani celebrities** with 180 images each.
* An additional **"others" class (-1)** with >540 images for unknown faces.
* Each image is labeled by **gender** and **name ID**.

```
/dataset
    /train
        /0 (celebrity ID)
        /1
        ...
        /14
        /-1 (others)
```

---

## 🧠 Models Used

### 1. **YOLOv8m**

* Used for **face detection** and **gender classification**.
* Trained on labeled images with bounding boxes and gender annotations.

### 2. **Keras ResNet50**

* Fine-tuned on YOLO-cropped face images.
* Used for **name classification** of known celebrities.

---

## 🧪 Pipeline

1. **Face Detection + Gender Classification**
   → Using YOLOv8m to detect faces and classify gender.

2. **Face Cropping**
   → Detected faces are cropped and passed to the next stage.

3. **Name Classification**
   → Cropped face is fed to ResNet50 model to predict celebrity identity.

---

## 📊 Evaluation Metrics

* **Gender Classification (YOLOv8):**

  * Precision, Recall, mAP
* **Name Classification (ResNet50):**

  * Top-1 Accuracy
  * Top-3 Accuracy
  * F1 Score, Precision, Recall

---
Example:
<img width="603" height="414" alt="image" src="https://github.com/user-attachments/assets/1b5f44f5-655c-4e6c-b7dd-8e0ecec2aff1" />

---



## 🧠 Future Work

* Extend dataset with more celebrities.
* Deploy as a web or mobile app.
* Improve classification with ensemble models.

---

## 🏆 Credits

* YOLOv8 by [Ultralytics](https://github.com/ultralytics/ultralytics)
* ResNet50 via [TensorFlow Keras](https://www.tensorflow.org/api_docs/python/tf/keras/applications/ResNet50)

---
