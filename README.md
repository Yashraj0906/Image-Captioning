🖼️ Image Captioning using CNN (ResNet50) + LSTM
📘 Overview

This project focuses on automatically generating captions for images using a combination of a Convolutional Neural Network (ResNet50) for visual feature extraction and an LSTM network for sequence generation.
The dataset used for this project is Flickr8k, which contains over 8,000 images each paired with five textual descriptions.

I trained and evaluated the model on Kaggle, utilizing GPU acceleration for faster training. The work demonstrates how deep learning can bridge the gap between computer vision and natural language processing.

🧠 Model Architecture

Feature Extractor: ResNet50 pretrained on ImageNet (last 20 layers unfrozen for fine-tuning)

Sequence Model: LSTM network with embedding and dropout layers

Fusion Mechanism: Concatenation of CNN features and LSTM output

Output: Softmax layer predicting the next word in the caption sequence

📊 Dataset

Dataset Used: Flickr8k (publicly available dataset on Kaggle)

Each image has five captions

Training and evaluation were done on Kaggle; some supporting files (.h5, .pkl, .txt) were not downloaded after training

🚀 How to Run
# Clone this repository
git clone https://github.com/<your-username>/Image-Captioning.git


(Make sure to add your Kaggle dataset path in the notebook before running.)

📈 Results

After training and evaluating the model, the following BLEU scores were obtained on a subset of the Flickr8k dataset:

BLEU-1 (subset): 0.183810
BLEU-2 (subset): 0.100456


These scores indicate that the model has learned basic word associations between image content and captions, with potential for improvement through extended training or larger datasets.

🧩 Key Features

CNN-LSTM hybrid model for image captioning

ResNet50 fine-tuned for better feature extraction

Efficient data generator for training on large image-caption pairs

BLEU metric for caption quality evaluation

🏷️ Tech Stack

Python

TensorFlow / Keras

NumPy, Pandas, Matplotlib

NLTK for text processing