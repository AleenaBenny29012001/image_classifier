MODEL SUMMARY:
A CNN (Convolutional Neural Network) was chosen to classify the images. CNNs are commonly used to analyse satellite imagery, medical images, time series data, and detect anomalies. They are effective at extracting features from data using multiple layers.

CNNs have three main components:
Convolution Layers:
•	Extract features from the input data.
•	Use filters or kernels to detect specific patterns in the image.
•	Slide the filter across the image and calculate dot products to generate a feature map.

Activation Functions:
•	Introduce non-linearity into the model.
•	Common activation functions include ReLU (Rectified Linear Unit) and sigmoid.

Pooling Layers:
•	Reduce the number of parameters in the input data.
•	Two main types: max pooling and average pooling.

Training Process:
1.	Image Processing:

•	Load and convert images to RGB color space.
•	Resize images to a uniform size.
•	Convert images into NumPy arrays.

2.	Model Architecture:

	Sequential CNN model with multiple layers:

•	Convolutional layer with 32 filters, 3x3 kernel, and ReLU activation.
•	Max-pooling layer with 2x2 pool size.
•	Flatten layer to transform 2D feature map into 1D vector.
•	Dense layer with 256 units and ReLU activation.
•	Dropout layer to prevent overfitting.
•	Dense layer with 512 units and ReLU activation.
•	Output layer with 5 units and softmax activation for multi-class classification.

3.	Model Compilation:

•	Compile the model using Adam optimizer, sparse categorical cross-entropy loss, and accuracy metric.

4.	Model Training:

•	Split the dataset into training (70%) and testing (30%) sets.
•	Normalize both training and testing data.
•	Train the model over 200 epochs with a 0.1 validation split.

Insights:
•	The model achieved an impressive 84% accuracy on the test set.
•	The model's performance may be limited by the small dataset size (150 images).
•	To improve performance, consider expanding and diversifying the training dataset and experimenting with regularization methods.

