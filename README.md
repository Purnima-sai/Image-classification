# 🦁🐘 Lion vs Elephant Image Classifier

This project uses **Convolutional Neural Networks (CNN)** with **TensorFlow/Keras** to classify images as either **Lion** or **Elephant**. It's built and tested on **Google Colab**, using a custom dataset of animal images stored in Google Drive.

## 📁 Project Structure
lion-elephant-classification/
│
├── training/
│ ├── lion/
│ └── elephant/
│
├── testing/
│ ├── lion/
│ └── elephant/
│
├── image-classification-testing.ipynb
├── model.h5 # (Optional: saved model)
└── images (3).jpg # test image

---

## 🚀 How It Works

### 1. **Data Augmentation & Loading**
Uses `ImageDataGenerator` to:
- Rescale pixel values
- Apply random transformations (flip, zoom, rotation)
- Load and label images from directories

### 2. **Model Architecture**
A simple CNN with:
- Conv2D + MaxPooling layers
- Flatten
- Dense layer
- Output layer with **sigmoid** activation for binary classification

```python
model = Sequential()
model.add(Conv2D(64, kernel_size=(3,3), activation='relu', input_shape=(64,64,3)))
model.add(MaxPooling2D(pool_size=(2,2)))
model.add(Flatten())
model.add(Dense(128, activation='relu'))
model.add(Dense(1, activation='sigmoid'))
✅ Requirements
pip install tensorflow keras numpy matplotlib
