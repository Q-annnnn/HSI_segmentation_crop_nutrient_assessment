# Crop nutrient fertilizer assessment system using Deep learning and Hyperspectral image

## Description
This project, conducted by myself and my group members, served as the culmination of our efforts for the "Group Project" subject at the University of Science and Technology of Hanoi. The primary objective was to develop a deep learning segmentation model capable of analyzing hyperspectral images to assess the nutrient content, specifically phosphorus, in fertilizers. The model provides an output indicating whether the phosphorus level in a given area is deficient, surplus, or sufficient based on standards set by agricultural experts.

To achieve this goal, a 3-D Unet model was employed, utilizing technologies such as the Python programming language and related support libraries like Spectral, TensorFlow, and Keras. The software LabelMe was utilized to generate ground truth images.

## Usage
The dataset consists of a hyperspectral image containing 122 bands. Due to information security and legal issues, the hyperspectral image data cannot be shared. However, users can substitute personal datasets and modify the code to suit specific requirements. The ground truth label image, indicating the fertilizer condition in each area, is created using LabelMe. A representation of the ground truth label image is shown below:
With the last band of the image:

<div align="center"><img src="img\label_viz.png"/></div>

The groundtruth used:

<div align="center"><img src="img\label.png"/></div>

## Detail Actions
Upon preprocessing and observation, the hyperspectral image data was deemed too large for the model's input (144x144). To address this, both the training image and the corresponding ground truth image were cropped to an appropriate shape, preventing the loss of important information. Principal Component Analysis (PCA) was implemented to optimize storage and enhance computational performance.

The set of cropped images was then divided into training, testing, and validation sets for the model to learn and be evaluated. The provided source code serves as an example for training a cropped image and evaluating accuracy based on the Intersection over Union (IoU) score.

## Result
The ground truth and predicted mask of the model (positioned at x = 4176, y = 4276 according to the original image) are visualized below:
Ground Truth:

<div align="center"><img src="img\gt.png"/></div>

Predicted Mask:

<div align="center"><img src="img\predicted_mask.png"/></div>

## Contributors
Special thanks to the USTH teachers for collecting the data and providing necessary information for this project; Dr. Tran Giang Son for being our supervisor in this project.

