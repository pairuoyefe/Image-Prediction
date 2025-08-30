# Image Classification with TensorFlow

##  Project Overview  
This project focuses on building an **image classification model** using **TensorFlow and Keras** to classify animals into four categories:  

- Camel  
- Dolphin  
- Horse  
- Zebra  

The project demonstrates **data preprocessing, model training, evaluation,** and making predictions on new images.  

---

##  Dataset  
- **Source**: Custom dataset with 1140 images across 4 classes.  
- Images were resized to **256 × 256 pixels**.  
- Data was split into **train (70%)**, **validation (15%)**, and **test (15%)** sets.  

---

##  Workflow  

### Data Preprocessing  
- Normalized pixel values (0–1).  
- Shuffled dataset for randomness.  
- Split into train/val/test sets.  

---

## Training
- **Optimizer**: Adam  
- **Loss Function**: Sparse Categorical Crossentropy  
- **Epochs**: 10  

## Results
- **Validation Accuracy**: ~100%  
- **Test Accuracy**: ~100%  
- **Model Saved Formats**: `.keras` and `.h5`  

### Example Predictions
- `Equus_quagga_burchellii_-_Etosha,_2014.jpg` → **Predicted: zebra**  
- `images (31).jpeg` → **Predicted: camel**  

## Recommendations
- Apply **data augmentation** (rotation, zoom, flip, shift) to improve model generalization.  
- Train on **cloud platforms** (Google Colab, Kaggle, Azure ML, AWS Sagemaker) for more computing power.  
- Use **transfer learning** (ResNet, MobileNet, EfficientNet) to improve performance with small datasets.  
- Expand the dataset by **scraping additional images** from online sources.  
- Perform **cross-validation** to confirm model stability and prevent overfitting.

- <img width="301" height="404" alt="image" src="https://github.com/user-attachments/assets/50d9ed41-f5dc-4da6-9ae5-cd74533cc1e9" />

<img width="459" height="299" alt="acimage" src="https://github.com/user-attachments/assets/d028c3d1-96d0-4b69-9b9d-8ec57317601a" />

### Model Architecture  
```python
model = keras.Sequential([
    layers.Input(shape=(256, 256, 3)),
    layers.Conv2D(32, (3, 3), activation='relu'),
    layers.MaxPooling2D(),
    layers.Conv2D(64, (3, 3), activation='relu'),
    layers.MaxPooling2D(),
    layers.Flatten(),
    layers.Dense(128, activation='relu'),
    layers.Dense(num_classes, activation='softmax')
])




         
