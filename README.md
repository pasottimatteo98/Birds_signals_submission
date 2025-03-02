# BirdSense: Multi-Modal Bird Species Recognition System

This repository contains a comprehensive bird species analysis system with three main components:
1. **Image Classification** - Identifying bird species from images
2. **Audio Classification** - Recognizing birds by their calls and songs
3. **Image Retrieval** - Finding similar bird images using feature extraction and similarity measures

## Project Overview

The project utilizes deep learning techniques to analyze and classify birds through different modalities. The system includes several pre-trained models and provides interactive demos for real-time classification and retrieval.

### Key Features

- Bird species classification from images using InceptionV3 transfer learning
- Audio classification of bird songs and calls using deep learning
- Image retrieval system to find similar bird images
- Grad-CAM visualization to understand model focus areas
- Interactive demo interfaces for all components

## Data

The project uses the following datasets:
- **Images**: "100-bird-species" dataset from Kaggle containing 525 different bird species
- **Audio**: Custom dataset of bird calls organized by species

## Components

### 1. Image Classification

The image classification system uses a fine-tuned InceptionV3 model with the following architecture:
- Pre-trained InceptionV3 base model (trained on ImageNet)
- Global Average Pooling layer
- Dropout layer (0.3) for regularization
- Dense output layer with softmax activation for 525 bird classes

#### Model Performance
- Test set accuracy: 85.5%
- Precision: 80%+
- Recall: 80%+
- F1-score: 85.2%

### 2. Audio Classification

The audio classification component processes bird songs through:
- Audio preprocessing and segmentation
- Mel-spectrogram generation
- Classification using a custom CNN architecture

#### Audio Model Architecture
- Multiple convolutional layers with batch normalization
- Global Average Pooling
- Dense layers with dropout for regularization
- Output layer with softmax activation

#### Performance
- Test set accuracy: 60%
- F1-score: 40.5% on handcrafted test set

### 3. Image Retrieval System

The retrieval system uses feature extraction to find similar bird images:
- Feature extraction using InceptionV3
- Cosine similarity measurement
- Grad-CAM visualization to highlight important regions

## Installation and Setup

### Prerequisites
- Python 3.7+
- TensorFlow 2.x
- Keras
- librosa
- pandas
- numpy
- matplotlib
- scikit-learn
- PIL/Pillow

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/bird-analysis-project.git
cd bird-analysis-project

# Install dependencies
pip install -r requirements.txt

# Download necessary models and data
python download_assets.py
```

## Usage

### Image Classification Demo

```python
python demo.py --mode image --image path/to/bird_image.jpg
```

### Audio Classification Demo

```python
python demo.py --mode audio --audio path/to/bird_call.ogg
```

### Image Retrieval Demo

```python
python demo.py --mode retrieval --image path/to/query_image.jpg
```

## Interactive Demo

The project includes an interactive demo with a web interface:

```bash
python interactive_demo.py
```

Navigate to `http://localhost:8080` in your browser to access the interactive demo.

## Files and Structure

- `retrival.py` - Implementation of the image retrieval system
- `evaluation.py` - Evaluation metrics and testing for audio classification
- `evaluation (1).py` - Evaluation metrics and testing for image classification
- `modeling.py` - Audio model architecture and training
- `modeling (1).py` - Image model architecture and training
- `demo.py` - Interactive demo application

## Results and Evaluation

### Image Classification
The image classifier achieved 85.5% accuracy on the test set, with precision and recall both above 80%. The model performs particularly well on distinctive species but struggles with visually similar birds.

### Audio Classification
The audio classifier achieved 60% accuracy on the test set. Performance varies significantly across species, with some birds being consistently recognized while others presenting challenges.

### Grad-CAM Visualization
Grad-CAM visualizations show that the model focuses on distinctive features such as:
- Beaks
- Wing patterns
- Distinctive coloration
- Head features

## Future Work

- Improve audio classification accuracy through more sophisticated architectures
- Expand the dataset to include more species and variations
- Implement ensemble methods to combine audio and visual classifications
- Develop a mobile application for field identification

## Acknowledgments

- Kaggle for providing the "100-bird-species" dataset
- TensorFlow and Keras teams for the deep learning framework
- The bird watching community for domain expertise and data collection
