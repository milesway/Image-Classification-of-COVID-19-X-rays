# Image-Classification-of-COVID-19-X-rays

The coronavirus has become the most urgent problem facing humanity. This project aims to classify X-ray images. We will use constrained data sets to explore the feasibility and difficulty of building a system that can classify different phenomena in chest X-rays images.


The data we will use has been collected by Adrian Xu, combining the Kaggle Chest X-ray dataset with the COVID-19 Chest X-ray dataset collected by Dr. Joseph Paul Cohen of the University of Montreal.
The datasets contain two separate parts, one for task 1 and the other for task 2. Each of them has been splitted into two parts, test and train. For task 1, each image is labeled by its causes: covid and normal. For task 2, each image is labeled by its causes: covid, normal, pneumonia bacteria, and pneumonia virus.

Task 1:
We start from taking a pre-trained model, VGG16 network, with weights obtained by training on Imagenet, and with the image size 224 x 224. We add a fully-connected layer with 256 neurons to allow processing on the entire image, and we use sigmoid function for binary classification with its confident value.

Optimizer: Adam

Loss function: binary cross-entropy Learning rate: 0.0005

Batch size: 10

Number of Epochs: 40

Image size = 224 x 224


Task 2:
We start from taking a pre-trained model, VGG16 network, with weights obtained by training on Imagenet, and with the image size 224 x 224. We add a fully-connected layer with 256 neurons to allow processing on the entire image, attached with the softmax activation function, since this will allow us to give a probability output for each of the classes, and eventually get the maximum as our final predicted output.

Optimizer: Adam

Loss function: categorical cross-entropy Learning rate: 0.0001

Batch size: 10

Number of Epochs: 100

Image size = 224 x 224
