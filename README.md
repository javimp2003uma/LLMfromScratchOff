# Building a Language Model from Scratch with PyTorch 🚀

![Language Model](https://c6140bba-5c2d-4e7d-a82a-e7f61c4f4b4e.s3.ap-southeast-2.amazonaws.com/blog/7/AI+Brain.jpeg)

## Overview

Welcome to the **Language Model from Scratch** project! This repository is dedicated to the development of a sophisticated language model designed for advanced text understanding and generation. Using PyTorch and other essential libraries, our goal is to build a robust model capable of processing and generating human-like text with high accuracy. This project encompasses all stages of model development, including data preprocessing, architecture design, training, evaluation, and deployment.

## Features ✨

- **Custom Model Architecture**: Implementation of state-of-the-art neural network architectures tailored for Natural Language Processing (NLP) tasks.
- **Efficient Data Handling**: Techniques for efficient data loading, preprocessing, and augmentation to handle large-scale text datasets.
- **Comprehensive Training Pipeline**: A complete training pipeline featuring batching, gradient clipping, learning rate scheduling, and model checkpointing to ensure robust model training.
- **Robust Evaluation Metrics**: A comprehensive suite of evaluation metrics to assess model performance across language modeling, text generation, and classification tasks.
- **Seamless Inference and Deployment**: Tools and scripts for model inference and deployment, including API integration and real-time text generation capabilities.

## Table of Contents 📑

- [Installation](#installation)
- [Usage](#usage)
- [Data](#data)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Evaluation](#evaluation)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Installation 💻

1. Clone the repository:
   
    ```sh
    git clone https://github.com/javimp2003uma/LLMfromscratch
    ```
3. Navigate to the project directory:
   
    ```sh
    cd LLMfromscratch
    ```
6. (Optional) Create a virtual environment:

   ```sh
    python -m venv venv
    .\venv\Scripts\activate  # On macOS/Linux use 'python -m venv venv
                                                   source venv/bin/activate'
    ```

5. Select venv as your python interpreter (in VSC):
   
    ```sh
    > Python: Select Interpreter
    .\venv\Scripts\python.exe # On macOS/Linux use './venv/bin/python'
    ```
8. Install the required packages:
   
    ```sh
    pip install -r requirements.txt
    ```

7. If you want to do a pull request which implies adding more dependencias, remember to update the requirements file using:
   
    ```sh
    pip freeze > requirements.txt
    ```

## Usage 📜

Details on how to use the model for training, evaluation, and inference will be provided in this section. Instructions include command-line usage, sample scripts, and API integration guidelines.

## Data 📊

The dataset used for training and evaluation is specifically curated for the domain of animal nutrition. It includes a comprehensive collection of questions and answers related to various aspects of animal nutrition, including dietary requirements, nutrient functions, and metabolic processes.

### Dataset Details

- **Source**: The dataset consists of text data extracted from scientific literature and educational resources on animal nutrition.
- **Preprocessing**: Text data has been cleaned and formatted to ensure consistency and remove any irrelevant information. Key preprocessing steps include tokenization, normalization, and handling special characters.
- **Format**: The dataset is structured in a question-answer format, with each entry consisting of a question followed by a detailed answer. The data is provided in JSON format for ease of use.
- **Example Entry**:
    ```json
    {
      "question": "What are the main components of foods, plants, and animals?",
      "answer": "The main components include water, dry matter, carbohydrates, lipids, proteins, nucleic acids, organic acids, vitamins, and minerals."
    }
    ```

## Model Architecture 🧠

The model is designed with a custom architecture optimized for understanding and generating text related to animal nutrition. 

### Key Components

- **Embedding Layers**: Transform input tokens into dense vectors.
- **Transformer Blocks**: Use multi-head self-attention and feed-forward layers to capture complex patterns in the text.
- **Positional Encoding**: Add positional information to token embeddings to account for the order of tokens.
- **Output Layers**: Generate probabilities for each token in the vocabulary based on the model's understanding of the input context.

### Configuration

The model's architecture and hyperparameters are specified in configuration files located in the `config` directory. Key parameters include the number of transformer layers, the size of the embedding vectors, and the number of attention heads.

## Training 🏋️‍♀️

Training the model involves several key steps to ensure optimal performance.

### Training Pipeline

1. **Data Loading**: Efficient loading and batching of data to handle large datasets.
2. **Loss Calculation**: Use cross-entropy loss to measure the difference between predicted and actual tokens.
3. **Optimization**: Employ techniques such as gradient clipping and learning rate scheduling to enhance training stability.
4. **Checkpointing**: Save model checkpoints at regular intervals to allow resuming training or evaluating different stages.

## Deployment 🚀

There are 3 Jupyter notebooks on the project. Once the libraries and depencies are ready (requierements.txt), you can run the notebooks and see the results. At the end of the last one, the model trained is exported into your machine has GPTtrained.pth, as Pytorch model files are supossed to.

## Contributing 🤝

I welcome contributions to this project! Please refer to our [contributing guidelines](CONTRIBUTING.md) for information on how to submit pull requests, report issues, and adhere to our code of conduct.
