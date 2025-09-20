# face-mask-detection-cnn
A deep learning project using Convolutional Neural Networks (CNN) to classify images as "With Mask" or "Without Mask".
The model can classify images of people into two categories:
- With Mask
- Without Mask
It is built using Python and TensorFlow/Keras
#Folder Structure
face-mask-detection-cnn/
|-face_mask_detection1.ipynb
|-requirements.txt
|-README.md
|-samples/
|-test2.jpg
|-test6.jpg
|-screenshot(1).jpg
|-scrrenshot(2).jpg
|-graph1.jpg
|-graph2.jpg

#Dataset

The dataset for this project is from Kaggle: [Face Mask Dataset](https://www.kaggle.com/omkargurav/face-mask-dataset).

### Steps to use the dataset:

1. Go to the Kaggle link above and download the dataset manually, or use Kaggle API:
    - Save your `kaggle.json` API key file (from your Kaggle account) on your machine.
    - Place it in the correct location:
      ```bash
      mkdir -p ~/.kaggle
      cp kaggle.json ~/.kaggle/
      chmod 600 ~/.kaggle/kaggle.json
      ```
    - Download the dataset using:
      ```bash
      kaggle datasets download -d omkargurav/face-mask-dataset
      ```
2. Extract the downloaded zip file into a folder called `data/` inside your project:
    ```python
    from zipfile import ZipFile

    with ZipFile('face-mask-dataset.zip', 'r') as zip:
        zip.extractall('data')
    ```
3. After extraction, your folder structure should look like this:
data/
with_mask/
without_mask/


> **Note:** Do not upload the dataset or `kaggle.json` to GitHub. Users should download it themselves.



#Model Architecture

The CNN model used in this project has the following layers:

Conv2D → activation: relu

MaxPooling2D

Conv2D → activation: relu

MaxPooling2D

Flatten

Dense → activation: relu

Dropout → 0.5

Dense → activation: sigmoid (binary classification)

Compiled with:

model.compile(optimizer='adam', loss='binary_crossentropy', metrics=['accuracy'])



#How to Run the Project

#Clone the repository:

git clone https://github.com/sneha456/face-mask-detection-cnn.git

#Install required libraries:

pip install -r requirements.txt

#Open the Notebook:

Open face_mask_detection.ipynb in Jupyter Notebook or Google Colab.

Run the Notebook:

Follow the steps to train the model or test predictions on sample images.

If the trained model file is not included, the notebook will train the model automatically.
Sample Images

The samples/ folder contains example images:

test6.jpg → Person wearing a mask
test2.jpg → Person not wearing a mask

graph1.jpg
graphh2.jpg
→ Graph showing training accuracy 
screenshot(1).jpg 
screenshot(2).jpg
->prediction

These samples help visualize how the model works.

#Requirements

All Python dependencies are listed in requirements.txt.

#Notes

The trained model file (face-mask_model.h5) is not included due to size limits.

Users need to download the dataset to run the notebook.

#Technologies Used

Python

TensorFlow / Keras

OpenCV

Matplotlib

Google Colab




pip install -r requirements.txt

