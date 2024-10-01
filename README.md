### **ANN-mnist.ipynb**:
1. **Install TensorFlow**:
   - Install the TensorFlow library using `pip install tensorflow`.

2. **Load Dataset**:
   - Load the **MNIST** dataset (handwritten digits) using NumPy.

3. **Visualize Data**:
   - Use Matplotlib to visualize a sample image from the dataset.

4. **Data Preprocessing**:
   - Normalize the pixel values of images to a range of 0 to 1.
   - One-hot encode the labels to create a classification-friendly format.

5. **Build the Neural Network**:
   - Create a sequential model with multiple layers:
     - **Flatten Layer**: Convert 28x28 images into 1D vectors.
     - **Dense Layers**: Add fully connected layers with ReLU activation.
     - **Output Layer**: Add a layer with softmax activation to classify the 10 digits.

6. **Compile the Model**:
   - Compile the model using the **Adam optimizer** and **categorical cross-entropy** loss function.

7. **Train the Model**:
   - Train the neural network for 10 epochs, using a batch size of 32 and a validation split of 0.2.

8. **Plot Training and Validation Curves**:
   - Visualize the loss and accuracy curves during training and validation to monitor performance.

9. **Test Predictions**:
   - Select random images from the test set and use the trained model to predict their labels.
   - Plot the images with their true and predicted labels using Matplotlib.

### Steps for **ANN-fashion-mnist.ipynb**:
The steps are the same as above, but instead of the **MNIST dataset**, the **Fashion MNIST** dataset is used. The model is built and trained to classify fashion items (e.g., shirts, shoes) instead of digits.

### CNN File

1. **Import necessary libraries:**
   - `numpy`, `tensorflow`, and `matplotlib` for handling data, building the model, and plotting images.
   - CNN-related functions (`Conv2D`, `Flatten`) are imported from `tensorflow.keras`.

2. **Load and prepare the MNIST dataset:**
   - The dataset contains handwritten digit images and corresponding labels (0–9 digits). 
   - `x_train` and `y_train` are used for training, while `x_test` and `y_test` are used for testing.

3. **Data preprocessing:**
   - **Normalize the images** by dividing the pixel values by 255 to scale them between 0 and 1.
   - **One-hot encode** the labels using `to_categorical` so that each digit is represented as a binary vector (0-9).

4. **Define the CNN model architecture:**
   - **Convolutional layers (Conv1D):** Learn features by applying filters (kernels) over the image to extract relevant patterns.
   - **Flatten layer:** Converts the 2D output from convolutional layers into a 1D vector to be input into a fully connected layer.
   - **Dense layer:** Final output with a softmax activation to classify images into one of the 10 digit classes.

5. **Compile the model:**
   - Loss function: `CategoricalCrossentropy`.
   - Optimizer: `Adam`.
   - Metric: `Accuracy`.

6. **Train the model:**
   - The model is trained for 5 epochs, using `x_train` and `y_train` for training and validating on the test data.

7. **Plot training and validation curves:**
   - Plot the training and validation loss and accuracy to visualize the model's performance over epochs.

8. **Evaluate the model:**
   - Randomly select 50 test images and predict their labels using the trained model.
   - Plot these images alongside the true and predicted labels.
