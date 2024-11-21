# English to Hindi Neural Machine Translation Model

## Overview
This repository contains a Neural Machine Translation (NMT) model designed to translate English sentences into Hindi. The model uses an encoder-decoder architecture with Long Short-Term Memory (LSTM) layers and is trained on the **Hindi-English Truncated Corpus** dataset.

**Key Features**:
- Data preprocessing for text normalization and tokenization.
- Custom batch generator for memory-efficient training.
- Encoder-Decoder architecture with embedding layers.
- Trained using the Keras deep learning framework.

---

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Setup](#setup)
- [Training](#training)
- [Model Checkpoints](#model-checkpoints)
- [Contributing](#contributing)

---

## Dataset
The **Hindi-English Truncated Corpus** dataset is used for training the model. The dataset contains English and Hindi sentence pairs, sourced from TED talks. Only sentences with a maximum length of 20 words are used for training.

### Preprocessing Steps:
1. Convert all text to lowercase.
2. Remove special characters, numbers, and extra spaces.
3. Add `START_` and `_END` tokens to Hindi sentences for better decoding.

---

## Model Architecture
The model is built using the **Encoder-Decoder** architecture with the following components:
- **Encoder**: 
  - Embedding layer for English sentences.
  - LSTM layer to generate context vectors (hidden and cell states).
- **Decoder**:
  - Embedding layer for Hindi sentences.
  - LSTM layer initialized with encoder states.
  - Dense layer with a softmax activation for predicting the target words.

---

## Setup
### Prerequisites
Ensure you have the following installed:
- Python 3.7 or later
- TensorFlow/Keras
- Numpy
- Pandas
- Matplotlib
- Seaborn

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/mbithesss/Language-Translation-with-Deep-Learning.git
   cd english-to-hindi-translation

2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
---

## Training
The model is trained using the following parameters:
- **Optimizer**: RMSprop
- **Loss Function**: Categorical Crossentropy
- **Batch Size**: 128
- **Epochs**: 100

Checkpoints are saved after every epoch to ensure progress is not lost.

---

## Model Checkpoints
Checkpoints are stored in `checkpoints.h5` directory. To load a checkpoint:
```python
model.load_weights('/checkpoint.h5')
```

---

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.

### Steps to Contribute
1. Fork the repository.
2. Create a new branch: 
   ```bash
   git checkout -b feature-branch
   ```
3. Commit your changes and push them to your fork:
   ```bash
   git push origin feature-branch
   ```
4. Open a pull request.





