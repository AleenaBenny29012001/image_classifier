MODEL SUMMARY:

A Convolutional Neural Network (CNN) was employed for image classification. CNNs are powerful for image analysis, extracting features through convolutional layers, introducing non-linearity with activation functions, and reducing parameters via pooling layers.
MODEL ARCHITECTURE:
Layer 1: Conv2D
    - Filters: 32
    - Kernel Size: (3, 3)
    - Activation: ReLU
Layer 2: MaxPooling2D
    - Pool Size: (2, 2)
Layer 3: Flatten
Layer 4: Dense
    - Units: 256
    - Activation: ReLU
Layer 5: Dropout
    - Rate: 0.5
Layer 6: Dense
    - Units: 512
    - Activation: ReLU
Layer 7: Dense (Output)
    - Units: 5 (for multi-class classification)
    - Activation: Softmax
MODEL COMPILATION:
Optimizer: Adam
Loss Function: Sparse Categorical Cross-Entropy
Metrics: Accuracy
DATA PROCESSING:
1. Image Loading and Conversion:
    - Read and convert images to RGB.
    - Resize images to (128, 128).
    - Convert images to NumPy arrays.
2. Data Split:
    - Train-Test split with a ratio of 80:20.
3. Normalization:
    - Normalize pixel values in the range [0, 1].
MODEL TRAINING:
- Train for 300 epochs with a batch size of 128.
- Utilize 10% of the training data for validation.
MODEL EVALUATION:
- Evaluate the model on the test set.
- Report accuracy and generate a classification report.
MODEL PREDICTION:
- Demonstrate model prediction on a sample image.
INSIGHTS:
- The model achieved an accuracy of 82% on the test set.
- Considerations for improvement:
    - Expand and diversify the training dataset.
    - Experiment with regularization techniques to prevent overfitting.
