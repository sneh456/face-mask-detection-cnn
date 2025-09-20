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


1. **Clone the repository**:
```bash
git clone https://github.com/your-username/face-mask-detection-cnn.git



pip install -r requirements.txt

