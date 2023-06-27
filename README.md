
# Potential talents

## Background:

Our company develops innovative Artificial Intelligence and Computer Vision solutions that revolutionize industries. Machines that can see: We pack our solutions in small yet intelligent devices that can be easily integrated to your existing data flow. Computer vision for everyone: Our devices can recognize faces, estimate age and gender, classify clothing types and colors, identify everyday objects and detect motion. Technical consultancy: We help you identify use cases of artificial intelligence and computer vision in your industry. Artificial intelligence is the technology of today, not the future.

MonReader is a new mobile document digitization experience for the blind, for researchers and for everyone else in need for fully automatic, highly fast and high-quality document scanning in bulk. It is composed of a mobile app and all the user needs to do is flip pages and everything is handled by MonReader: it detects page flips from low-resolution camera preview and takes a high-resolution picture of the document, recognizing its corners and crops it accordingly, and it dewarps the cropped document to obtain a bird's eye view, sharpens the contrast between the text and the background and finally recognizes the text with formatting kept intact, being further corrected by MonReader's ML powered redactor.

MonReader is a new mobile document digitalization experience for the blind, for researchers and for everyone else in need for fully automatic, highly fast and high-quality document scanning in bulk. It is composed of a mobile app and all the user needs to do is flip pages and everything is handled by MonReader: it detects page flips from low-resolution camera preview and takes a high-resolution picture of the document, recognizing its corners and crops it accordingly, and it dewarps the cropped document to obtain a bird's eye view, sharpens the contrast between the text and the background and finally recognizes the text with formatting kept intact, being further corrected by MonReader's ML powered redactor.


## Data Description:

We collected page flipping video from smart phones and labelled them as flipping and not flipping.

We clipped the videos as short videos and labelled them as flipping or not flipping. The extracted frames are then saved to disk in a sequential order with the following naming structure: VideoID_FrameNumber

## Download Data:

https://drive.google.com/file/d/1KDQBTbo5deKGCdVV_xIujscn5ImxW4dm/view?usp=sharing

## Goal(s):

Predict if the page is being flipped using a single image.

## Success Metrics:

Evaluate model performance based on F1 score, the higher the better.

# Method and Results
## Exploratory data analysis
I first explored the data to gain insights. This included looking at how many entries we have:
total training flip images: 1162
total training not flip images: 1230
total testing flip images: 290
total testing not flip images: 307

This amounts to 51% not flippedimages and 19% testing data.

## Cleaning data 
I resized all images to 200x200

## Model
I defined different Convolutional Neural Network (CNN) model architectures including different numbers of convolutional layers (0 to 3) and different densities.
I then trained them to to see what led to a better accuracy and good F1 score.

## Conclusion

The best accuracy and f1 score were for the first iteration of the model (1 convolution layer, 1 maxpooling layer, 2 dense layers) with 98.8% accuracy, F1: 98.8%.

Without the convolution layer(s) and maxpooling, accuracy and f1 score were best when the density was 128, but didn't reach the accuracy of the first model.


