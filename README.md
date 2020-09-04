This is my solution for the Dog Breed Classifier Project in Udacity Deep Learning Nanodegree [original repo includes set up instructions](https://github.com/udacity/deep-learning-v2-pytorch/tree/master/project-dog-classification).

## Project Overview

Given an image, our algorithm will first tell whether it includes a human or a dog. If there is a dog detected, it will further tell its breed. If there is a human detected, it will tell its resembling dog breed.

## Details
This algorithm is achieved by appling a few models:
* To detect human faces in images, we use OpenCV's implementation of [Haar feature-based cascade classifiers](https://docs.opencv.org/trunk/d7/d8b/tutorial_py_face_detection.html).
* To detect dog in images, we use the VGG-16 model trained on image net.
* To predict dog breed, we developed a model through transfer learning from a pertained vgg16 model (reusing the feature layers while retraining the classifier layers on our training data).

## Note
* The dog_app.html is exported from dog_app.iypnb as html format for easy review purpose.
* We also build a CNN model from scratch and train on our dataset for dog breed classification in the notebook. We do it as an exercie but not used in the final algorithm due to its poor performance.
* /my_images folder includes my own data used for testing the algorithm.
