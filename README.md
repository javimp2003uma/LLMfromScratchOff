# Building a Language Model from Scratch with PyTorch 🚀

![Language Model](https://c6140bba-5c2d-4e7d-a82a-e7f61c4f4b4e.s3.ap-southeast-2.amazonaws.com/blog/7/AI+Brain.jpeg)

## Overview

Welcome to the **Language Model from Scratch** project! This repository is dedicated to the development of a sophisticated language model designed for advanced text understanding and generation. Using PyTorch and other essential libraries, our goal is to build a robust model capable of processing and generating human-like text with high accuracy. This project encompasses all stages of model development, including data preprocessing, architecture design, training, evaluation, and deployment. 

Before diving into the details, I would like to extend my gratitude to [Sebastian Raschka](https://www.linkedin.com/in/sebastianraschka) for his inspiring book *‘Build a Large Language Model’*. His work, along with various supporting documents and videos, has greatly contributed to the success of this project.

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
- [Deployment](#deployment)
- [Contributing](#contributing)
- [Bibliography](#bibliography)

## Installation 💻

1. Clone the repository:
   
    ```sh
    git clone https://github.com/javimp2003uma/LLMfromscratch
    ```
2. Navigate to the project directory:
   
    ```sh
    cd LLMfromscratch
    ```
3. (Optional) Create a virtual environment:

    ```sh
    python -m venv venv
    .\venv\Scripts\activate  # On macOS/Linux use 'source venv/bin/activate'
    ```

4. Select `venv` as your Python interpreter (in Visual Studio Code):
   
    ```sh
    > Python: Select Interpreter
    .\venv\Scripts\python.exe # On macOS/Linux use './venv/bin/python'
    ```
    ```
    source venv/bin/activate
    ```

5. Install the required packages:
   
    ```sh
    pip install -r requirements.txt
    ```

6. If you make changes that require additional dependencies, remember to update the `requirements.txt` file:
   
    ```sh
    pip freeze > requirements.txt
    ```
7. Once the principal installation has been done, you need to "tell" Jupyter where to find the kernel as follows ...
   ```sh
   python3 -m ipykernel install --user --name=venv --display-name "venvLLM" where venvLLM can be whatever you want
   ```

## Usage 📜

This section provides instructions for using the model. The repository is composed of 3 Jupyter notebooks where the concepts learned throughout the book are applied and developed. Particularly, the first 2 are part of the learning of basic concepts, although with the purpose of the project it is really important to execute them as well. The one that really develops and trains the model is trainingGPT.ipynb, which automatically executes the second one at startup.

## Data 📊

The dataset used for training and evaluation is curated for the domain of animal nutrition. It includes a comprehensive collection of questions and answers related to various aspects of animal nutrition, including dietary requirements, nutrient functions, and metabolic processes.

### Dataset Details

- **Source**: The dataset is derived from scientific literature and educational resources on animal nutrition. It is available as part of a HuggingFace repository for datasets [here](https://huggingface.co/datasets/A2H0H0R1/Animal-nutrition).
- **Preprocessing**: The text data has been cleaned and formatted to ensure consistency and remove irrelevant information. Key preprocessing steps include tokenization, normalization, and handling special characters.
- **Format**: The dataset is structured in a question-answer format, with each entry containing a question followed by a detailed answer. The data is provided in JSON format for ease of use.
- **Example Entry**:
    ```json
    {
      "question": "What are the main components of foods, plants, and animals?",
      "answer": "The main components include water, dry matter, carbohydrates, lipids, proteins, nucleic acids, organic acids, vitamins, and minerals."
    }
    ```

## Model Architecture 🧠

The model features a custom architecture optimized for understanding and generating text related to animal nutrition.

### Key Components

- **Embedding Layers**: Convert input tokens into dense vectors.
- **Transformer Blocks**: Utilize multi-head self-attention and feed-forward layers to capture complex text patterns.
- **Positional Encoding**: Incorporate positional information into token embeddings to account for token order.
- **Output Layers**: Produce probabilities for each token in the vocabulary based on the model's context understanding.

### Configuration

Model architecture and hyperparameters are specified in configuration files located in the `config` directory. Key parameters include the number of transformer layers, embedding vector size, and number of attention heads.

## Training 🏋️‍♀️

Training involves several key steps to ensure optimal performance.

### Training Pipeline

1. **Data Loading**: Efficiently load and batch data to manage large datasets.
2. **Loss Calculation**: Employ cross-entropy loss to measure the difference between predicted and actual tokens.
3. **Optimization**: Utilize gradient clipping and learning rate scheduling to enhance training stability.
4. **Checkpointing**: Save model checkpoints regularly to resume training or evaluate different stages.

## Deployment 🚀

The project includes three Jupyter notebooks. After setting up the libraries and dependencies (as specified in `requirements.txt`), you can run the notebooks to observe the results. At the end of the final notebook, the trained model is exported as `GPTtrained.pth`, which is the standard PyTorch model file format.

## Contributing 🤝

Contributions are welcome! Please refer to our [contributing guidelines](CONTRIBUTING.md) for details on submitting pull requests, reporting issues, and adhering to our code of conduct.

## Bibliography 📚

- [Transformer Architecture Explained](https://medium.com/@amanatulla1606/transformer-architecture-explained-2c49e2257b4c)
- [Attention is All You Need](https://arxiv.org/pdf/1706.03762)
- [YouTube Video on Transformer Architecture](https://www.youtube.com/watch?v=SZorAJ4I-sA)
- [AIML Explanation of Transformer Architecture](https://www.google.com/url?sa=i&url=https%3A%2F%2Faiml.com%2Fexplain-the-transformer-architecture%2F&psig=AOvVaw3_2WjOrzqsQ5favxNHs2eR&ust=1723633859023000&source=images&cd=vfe&opi=89978449&ved=0CBcQjhxqFwoTCKD3itHq8YcDFQAAAAAdAAAAABAE)

---

Thank you very much for visiting the repository of the project and I hope that if you are a beginner like me in the magnificent world of LLMs, this will serve as a push to start learning.
