
# Bone Age Prediction Using VGG19

This rep contains code for predicting bone age using X-ray images and a modified VGG19 model. The dataset (RSNA Bone Age) is preprocessed, normalized, and passed through a convolutional neural network to predict the bone age of patients.

## Dataset

The dataset used is the **RSNA Bone Age** available on Kaggle. Each image corresponds to a particular patient’s bone age, and the task is to predict the age based on X-ray images.

## Project Workflow

1. **Data Preprocessing:**
   - The `ImageDataGenerator` is used to apply data augmentation techniques such as rescaling, rotation, zooming, and flipping.

2. **Model Architecture:**
   - The pre-trained VGG19 model is loaded from Keras.
   - Custom convolutional layers are added to the pre-trained model to adjust it for bone age prediction.
   - The final output layer is a dense layer with linear activation to predict bone age.

3. **Model Compilation and Training:**
   - The model is compiled using the **Adam** optimizer with a learning rate of 0.0001.
   - The loss function used is `hinge` loss and the model is evaluated using **mean absolute error**.
   - Various callbacks such as **ModelCheckpoint**, **ReduceLROnPlateau**, and **EarlyStopping** are used to monitor training and adjust learning rates.

4. **Evaluation:**
   - The model’s predictions are plotted against the actual bone ages to assess accuracy.
   - Visualizations of predictions for sample X-ray images are generated and saved as PNG files.
   - An average deviation between the predicted and actual ages is calculated.


## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Ifrahaha/BoneAge-Custom-VGG19.git
   cd BoneAge-Custom-VGG19
   ```

2. Install the necessary libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Upload your dataset and adjust the dataset paths in the code:
   ```python
   base_bone_dir = '/path-to-your-dataset/'
   ```

## Dependencies

- Python 3.x
- TensorFlow/Keras
- NumPy, Pandas
- Matplotlib


