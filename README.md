# DL- Developing a Neural Network Classification Model using Transfer Learning

AIM
To develop an image classification model using transfer learning with VGG19 architecture for the given dataset.

THEORY
Transfer Learning is a technique where a pre-trained model (trained on a large dataset such as ImageNet) is used as a starting point for a different but related task. It leverages learned features from the original task to improve learning efficiency and performance on the new task.

VGG19 is a convolutional neural network with 19 layers. It consists of multiple convolutional layers for feature extraction, followed by fully connected layers for classification. In transfer learning, we typically freeze the convolutional layers and retrain the final fully connected layers to match our dataset.

Neural Network Model
VGG19 Architecture for Transfer Learning:

Input Image (224x224x3) │ [Convolution + ReLU] x multiple layers │ Max Pooling layers │ Flatten Layer │ Fully Connected Layer (4096) │ Fully Connected Layer (4096) │ Final Fully Connected Layer → num_classes (retrained) │ Softmax Activation → Class Probabilities

DESIGN STEPS
STEP 1: Load and Preprocess Dataset
Unzip the dataset and organize into train and test folders.
Resize all images to 224x224.
Convert images to tensors and optionally normalize them.
STEP 2: Load Pretrained Model
Load VGG19 model from torchvision.models.
Replace the last fully connected layer to match num_classes of your dataset.
STEP 3: Define Loss and Optimizer
Use CrossEntropyLoss for multi-class classification.
Use Adam optimizer to train only the final layer.
STEP 4: Train the Model
Freeze feature extractor layers.
Train only the final classifier for a few epochs.
Track training loss and validation loss for each epoch.
STEP 5: Evaluate the Model
Predict on the test set.
Compute accuracy, confusion matrix, and classification report.
STEP 6: Predict on New Samples
Select a test image.
Pass through the model and display predicted and actual class.




## PROGRAM

### Name:

### Register Number:

```python
# Load Pretrained Model and Modify for Transfer Learning



# Modify the final fully connected layer to match the dataset classes



# Include the Loss function and optimizer



# Train the model


```

### OUTPUT

## Training Loss, Validation Loss Vs Iteration Plot

Include your plot here

## Confusion Matrix

Include confusion matrix here

## Classification Report
Include classification report here

### New Sample Data Prediction
Include your sample input and output here

## RESULT
Include your result here
