# 🛣️ Parking detection

## 🚦 Overview  
This project leverages **computer vision** to detect parking spots and present available (empty) spots to drivers, helping them save time by avoiding the search for an empty spot. Using a comprehensive dataset of images from different parking areas, we trained and tested the **YOLOv8** model and integrated the **SAHI** model to enhance the accuracy of identifying empty parking spots.

---


### 🤖 Model Training   
#### YOLOv8 Model

- Epochs: 150
- Batch Size: 16
- Image Size: 640
- Target Classes:
    - Empty Spot
    - Equipped Spot (Occupied)


#### SAHI Model

The SAHI (Sliced Aided Hyper Inference) model was integrated to improve detection performance on large parking areas. It slices large images for better memory management and accuracy, especially in cases with overlapping or cluttered objects.


---

## 🏆 Results  
he best weights from training were used to test the model on a dedicated testing set, and the model was also evaluated for real-time detection in a video.
### Original Image
<img src="Screenshot (240).png" alt="winterm" width="450">

### Detection with YOLOv8 Only
<img src="Screenshot (239).png" alt="winterm" width="450">

### Detection with YOLOv8 + SAHI
<img src="Screenshot (238).png" alt="winterm" width="450">
