🖼️ Image Captioning using ResNet50 + LSTM 
📘 Overview

This project focuses on automatically generating captions for images using a hybrid deep learning architecture — a Convolutional Neural Network (ResNet50) for extracting visual features and a Long Short-Term Memory (LSTM) network for generating natural language descriptions.

The model was trained and evaluated on the Flickr8k dataset, which contains over 8,000 images, each paired with five captions.
Training and evaluation were performed on Kaggle with GPU acceleration for efficiency.
This work demonstrates how deep learning bridges the gap between Computer Vision and Natural Language Processing (NLP).

🧠 Model Architecture

Feature Extractor: ResNet50 pretrained on ImageNet (last 20 layers unfrozen for fine-tuning)

Sequence Model: LSTM network with embedding and dropout layers

Fusion Mechanism: Concatenation of CNN features and LSTM outputs

Output: Softmax layer predicting the next word in the caption sequence

📊 Dataset

Dataset Used: Flickr8k Dataset (Kaggle)

Each image has five textual captions

Training and evaluation were done on Kaggle

Some trained model files (.h5, .pkl, .txt) were not downloaded after completion

🛠️ Environment Setup
# Clone the repository
git clone https://github.com/Yashraj0906/Image-Captioning.git
cd Image-Captioning
(Make sure to update your Kaggle dataset path in the notebook before running.)

📈 Results

After training and evaluation, the model achieved the following BLEU scores on a subset of the Flickr8k dataset:

BLEU-1 (subset): 0.183810
BLEU-2 (subset): 0.100456


These results indicate that the model successfully learned basic semantic and syntactic relationships between images and their corresponding captions, with potential for improvement through longer training or larger datasets.

🧩 Key Features

CNN–LSTM hybrid architecture for end-to-end image captioning

Fine-tuned ResNet50 for improved visual understanding

Efficient data generator for memory-optimized training

BLEU score evaluation for caption quality measurement

🏷️ Tech Stack

Python

TensorFlow / Keras

NumPy, Pandas, Matplotlib

NLTK for text preprocessing
