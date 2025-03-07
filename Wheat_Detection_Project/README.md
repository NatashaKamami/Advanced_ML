# Wheat Detection Using Deep Learning

## Project Overview
This project focuses on object detection for wheat heads in images using deep learning techniques. The goal is to identify and localize wheat heads in images by training a deep learning model on annotated data. The dataset includes images with bounding box annotations indicating the presence of wheat heads.

## Dataset and Preprocessing
The dataset consists of images and corresponding bounding box annotations stored in a CSV file. The images are preprocessed and augmented to improve model generalization. Key preprocessing steps include:
- Resizing images to 128x128 pixels.
- Normalizing pixel values.
- Augmenting images using transformations such as rotation, zoom, and flipping.
- Parsing bounding box annotations and applying transformations to match augmented images.
- Splitting the dataset into training (80%) and validation (20%) sets.

## Model Architecture
The model is based on the MobileNetV2 architecture as a feature extractor, which is pretrained on ImageNet. Key layers include:
- A MobileNetV2 backbone for feature extraction.
- A flattening layer followed by dense layers.
- Two output layers:
  - A bounding box regressor to predict the coordinates (xmin, ymin, width, height).
  - A classifier to predict the presence of wheat heads.

## Training
The model is trained using a custom data generator that loads images and bounding boxes in batches. The training process includes:
- Using Mean Squared Error (MSE) for bounding box regression loss.
- Using Binary Cross-Entropy loss for classification.
- Applying Adam optimizer.
- Early stopping to prevent overfitting.

## Testing and Predictions
The trained model is used to predict bounding boxes on test images. Key steps include:
- Loading test images and preprocessing them.
- Passing images through the trained model to predict bounding boxes.
- Scaling bounding boxes to match the original image dimensions.
- Saving predictions in a CSV file for submission.

## Submission
The final predictions are saved in `submission.csv`, which contains:
- `image_id`: Unique identifier for the image.
- `bbox`: List of bounding box coordinates [xmin, ymin, width, height].

## Conclusion
This project successfully detects wheat heads in images using a deep learning-based object detection approach. The model leverages deep learning to achieve accurate predictions with minimal training data. 


