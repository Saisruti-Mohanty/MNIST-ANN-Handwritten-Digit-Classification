
# MNIST Handwritten Digit Classification using ANN

A Deep Learning project that uses an Artificial Neural Network (ANN) to recognize handwritten digits from the MNIST dataset.

---

## 📌 Project Overview

Handwritten digit recognition is a classic problem in Machine Learning and Computer Vision.

In this project, an Artificial Neural Network is trained using the **MNIST handwritten digit dataset** to classify images of handwritten digits into one of **10 classes (0–9)**.

The project demonstrates the complete Deep Learning workflow:

- Loading the MNIST dataset
- Exploring the dataset
- Visualizing handwritten digit images
- Preprocessing image data
- Normalizing pixel values
- Reshaping image data
- Encoding target labels
- Building an ANN using Keras Sequential
- Training the neural network
- Evaluating the model
- Visualizing training performance
- Predicting digits from custom images

---

## 🎯 Objective

The main objective of this project is to build an ANN model capable of recognizing handwritten digits.

Given an image containing a handwritten digit, the model predicts which digit it represents.

### Example

```text
Handwritten Image
       ↓
   Preprocessing
       ↓
      ANN
       ↓
   Prediction
       ↓
      Digit
````

The model performs **10-class classification**:

```text
0  1  2  3  4  5  6  7  8  9
```

---

## 📊 Dataset

The project uses the **MNIST handwritten digit dataset**.

MNIST contains grayscale images of handwritten digits ranging from **0 to 9**.

Each image has a resolution of:

```text
28 × 28 pixels
```

Each image is represented using pixel intensity values.

The dataset is divided into:

* Training data — used to train the neural network
* Testing data — used to evaluate the trained model on unseen images

---

## 🔍 Understanding the Images

Each MNIST image represents one handwritten digit.

For example:

```text
28 × 28 grayscale image
           ↓
     Pixel values
           ↓
      Handwritten
         digit
```

The pixel values contain information about the shape and structure of the handwritten digit.

The model learns patterns from these pixel values during training.

---

## 🔄 Data Preprocessing

Before feeding the images into the ANN, the data is preprocessed.

### 1. Pixel Normalization

The original pixel values are represented in the range:

```text
0 → 255
```

The pixel values are normalized to:

```text
0 → 1
```

This is done by scaling the pixel values.

Normalization helps the neural network train more efficiently because the input values are brought into a smaller and consistent range.

---

### 2. Reshaping the Images

The original MNIST images have dimensions:

```text
28 × 28
```

Since the project uses an Artificial Neural Network with dense layers, the 2D image needs to be converted into a 1D vector.

Therefore:

```text
28 × 28 = 784
```

So each image is converted from:

```text
28 × 28
```

to:

```text
784
```

input values.

---

### 3. Label Encoding

The target labels represent digits from:

```text
0 → 9
```

The labels are converted into categorical form using Keras utilities so that the neural network can perform multi-class classification.

---

## 🧠 Artificial Neural Network

The project uses a **Sequential model from Keras**.

The general architecture follows this workflow:

```text
MNIST Image
     ↓
Flattened Input
     ↓
Dense Layer
     ↓
Hidden Layer(s)
     ↓
Output Layer
     ↓
10 Classes
```

The output layer provides predictions for all ten possible digits:

```text
0  1  2  3  4  5  6  7  8  9
```

The class with the highest predicted probability is selected as the final prediction.

---

## ⚙️ Model Training

The ANN is trained using the MNIST training dataset.

During training, the neural network learns patterns from the pixel values of handwritten digits.

The model gradually learns features such as:

* Lines
* Curves
* Shapes
* Pixel arrangements
* Digit structures

The model's performance is monitored using loss and accuracy.

---

## 📈 Model Evaluation

The ANN model achieved the following performance during training:

| Metric | Training | Validation |
|---|---:|---:|
| Accuracy | **97.67%** | **96.83%** |
| Loss | **0.1013** | **0.1413** |

### Final Training Results

```text
Training Accuracy:   97.67%
Training Loss:       0.1013

Validation Accuracy: 96.83%
Validation Loss:     0.1413
## 📊 Training Visualization

The notebook includes visualizations of the model's training process.

The graphs can be used to observe:

### Accuracy

Training and validation accuracy show how the model's classification performance changes over the training process.

### Loss

Training and validation loss show how the model's error changes during training.

These plots can also help identify potential overfitting or underfitting.

---

## 🖼️ Custom Image Prediction

The project also includes a section for predicting a handwritten digit from a custom image.

This allows the trained ANN to be tested on an image outside the original MNIST test dataset.

### How to Test Your Own Image

#### Step 1 — Prepare an Image

Create or select an image containing a handwritten digit.

For best results, use a clear image containing a single digit.

#### Step 2 — Place the Image

Place your image in the project folder.

For example:

```text
MNIST-ANN-Handwritten-Digit-Classification/
│
├── MNIST_ANN.ipynb
├── your_digit.jpg
├── README.md
├── LICENSE
└── .gitignore
```

#### Step 3 — Update the Image Path

In the custom prediction section of the notebook, update the image path.

Example:

```python
image_path = "your_digit.jpg"
```

If the image is stored in another folder, provide the appropriate path.

#### Step 4 — Run the Prediction Cell

The image will be processed and passed to the trained ANN.

The general workflow is:

```text
Custom Image
     ↓
Image Loading
     ↓
Image Preprocessing
     ↓
Resizing
     ↓
Normalization
     ↓
Reshaping
     ↓
ANN Model
     ↓
Prediction
     ↓
Predicted Digit
```

### Example

```text
Input:
Handwritten image of 7

Output:
Predicted Digit: 7
```

> **Note:** Custom images may require appropriate preprocessing to match the format expected by the MNIST-trained model. Images that differ significantly in background, orientation, size, or writing style may produce incorrect predictions.

---

## 🛠️ Technologies Used

| Technology       | Purpose                                      |
| ---------------- | -------------------------------------------- |
| Python           | Programming language                         |
| NumPy            | Numerical operations                         |
| Matplotlib       | Data visualization                           |
| OpenCV           | Image processing and custom image prediction |
| TensorFlow       | Deep Learning framework                      |
| Keras            | Neural network development                   |
| Jupyter Notebook | Development environment                      |

---

## 📂 Project Structure

```text
MNIST-ANN-Handwritten-Digit-Classification/
│
├── MNIST_ANN.ipynb
├── README.md
├── LICENSE
└── .gitignore
```

---

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/Saisruti-Mohanty/MNIST-ANN-Handwritten-Digit-Classification.git
```

### 2. Navigate to the Project

```bash
cd MNIST-ANN-Handwritten-Digit-Classification
```

### 3. Install the Required Libraries

If the required packages are not already installed, install them using:

```bash
pip install numpy matplotlib opencv-python tensorflow
```

### 4. Launch Jupyter Notebook

Run:

```bash
jupyter notebook
```

Then open:

```text
MNIST_ANN.ipynb
```

### 5. Run the Notebook

Run the cells sequentially from top to bottom.

---

## 🧪 Project Workflow

The complete workflow of the project can be summarized as:

```text
MNIST Dataset
      ↓
Data Exploration
      ↓
Image Visualization
      ↓
Data Preprocessing
      ↓
Normalization
      ↓
Reshaping
      ↓
Label Encoding
      ↓
ANN Model Creation
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Accuracy & Loss Visualization
      ↓
Custom Image Prediction
```

---

## 📚 Key Concepts Learned

This project helped in understanding and practicing several important Deep Learning concepts:

* Understanding image datasets
* Grayscale image representation
* Pixel values
* Image normalization
* Image reshaping
* Categorical encoding
* Artificial Neural Networks
* Dense layers
* Sequential models
* Model training
* Loss functions
* Accuracy
* Model evaluation
* Training and validation curves
* Image preprocessing using OpenCV
* Making predictions using a trained model

---

## 🚀 Future Improvements

The project can be improved further by:

* Experimenting with different ANN architectures
* Trying different numbers of hidden layers
* Tuning the number of neurons
* Experimenting with different optimizers
* Improving custom image preprocessing
* Comparing ANN performance with a CNN
* Building a simple Streamlit interface
* Allowing users to upload an image and receive a digit prediction

---

## 🔮 ANN vs CNN

This project uses an **ANN** for handwritten digit classification.

A possible next step is to build a **Convolutional Neural Network (CNN)** for the same MNIST dataset.

A CNN is generally better suited for image-related tasks because it can learn spatial patterns in images more effectively.

A future comparison could be:

```text
MNIST Dataset
      ↓
 ┌───────────┐
 │           │
ANN         CNN
 │           │
 ↓           ↓
Accuracy   Accuracy
 │           │
 └─────┬─────┘
       ↓
 Performance Comparison
```

---

## 💡 Why This Project?

MNIST is a simple but important dataset for learning Deep Learning.

This project provides practical experience with the complete pipeline of an image classification problem:

```text
Data → Preprocessing → Model → Training → Evaluation → Prediction
```

It also provides a foundation for moving from basic Artificial Neural Networks to more advanced Computer Vision models such as CNNs.

---

## 👩‍💻 Author

**Saisruti Mohanty**

B.Tech – Computer Science & Data Science
SOA University, Bhubaneswar

---

## 📄 License

This project is licensed under the **MIT License**.

See the `LICENSE` file for more information.

---

## ⭐ Acknowledgement

This project was created as part of my learning journey in **Machine Learning, Deep Learning, and Computer Vision**.

The project focuses on understanding the fundamentals of Artificial Neural Networks and applying them to handwritten digit classification.

````


