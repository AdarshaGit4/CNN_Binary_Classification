# Cat vs. Dog Image Classification using a Convolutional Neural Network (CNN)

This project is a straightforward implementation of a CNN to distinguish between images of cats and dogs. The model is built using TensorFlow's Keras API and is trained on a dataset of cat and dog images.



---

## 📜 Description

The primary goal of this project is to build and train a CNN model that can accurately classify an input image as either a "cat" or a "dog." This project demonstrates the entire machine learning pipeline, from data preprocessing and augmentation to model building, training, and finally, making predictions on new images.

---

## 💾 Dataset

The model was trained and tested on a dataset of thousands of cat and dog images.

* **Training Set**: 8000 images
* **Test Set**: 2000 images

The `ImageDataGenerator` from Keras was used for image augmentation on the training data. This process, which included rescaling, shearing, zooming, and horizontal flipping, helps increase the diversity of the training set to prevent overfitting. The test set images were only rescaled.

---

## 🤖 Model Architecture

The CNN architecture is sequential and consists of the following layers:

1.  **Input Layer**: Expects images of size `(64, 64, 3)`.
2.  **Convolutional Layer 1**: 32 filters with a `(3,3)` kernel and 'relu' activation.
3.  **Max Pooling Layer 1**: A `(2,2)` pooling size.
4.  **Convolutional Layer 2**: 32 filters with a `(3,3)` kernel and 'relu' activation.
5.  **Max Pooling Layer 2**: A `(2,2)` pooling size.
6.  **Flatten Layer**: Converts the 2D feature maps into a 1D vector.
7.  **Dense Layer (Hidden)**: A fully connected layer with 128 units and 'relu' activation.
8.  **Dense Layer (Output)**: A single neuron with a 'sigmoid' activation for binary classification.

The model is compiled with the **Adam optimizer**, using **binary cross-entropy** as the loss function, and **accuracy** as the evaluation metric.

---

## ⚙️ Dependencies

To run this project, you will need the following libraries. You can install them using pip:

```bash
pip install tensorflow numpy
