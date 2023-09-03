# Image-Captions-Predictions
In this mini-project I'll take an image and their possible captions from the Flickr8k library and predict captions on images.

Using libraries: numpy, pandas, keras, pickle, tensorflow, matplotlib, nltk and more

First, I'll clean the raw data captions, and create a unique vocabulry of possible words. <br>
The train data will be the images and their captions, and the testing data wll be only the images. <br>
For the image preprocess I'll use ResNet50- a model to extract features from the train images, and than encode the images to one numerical vector.<br>
For the caption preprocess, I'll create a mapping between the encoded vetor to its translation into a sequence of words, and then use word embeddings- convert each word to a vector using the GloVe algorithm.<br>
The unique words will be loaded to the predictiong model in a form of an embedding matrix.

After all that, I'll create a predictive model with 2 parts- image and caption, that will be able to predict a probability for each word suggested to be in the caption for the image. <br>
To sum it up, I'll evaluate my model with the BLEU score- an algorithm for evaluating the quality of text which has been machine-translated from one natural language to another, with different weights (1-gram, 2-gram, 3-gram and 4-gram). <br>

Image dataset- https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_Dataset.zip <br>
GloVe algorithm (download as txt file- https://www.kaggle.com/datasets/watts2/glove6b50dtxt
