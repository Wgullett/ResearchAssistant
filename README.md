Research Assistant Notebook

This Jupyter Notebook (ResearchAssistant.ipynb) provides an interactive and efficient way to perform grounded question answering based on provided documents or blocks of text.

By leveraging the Mistral API, the assistant reads external context (like research papers, articles, or meeting notes) and accurately answers specific questions, ensuring the response is directly supported by the provided source material.

Features

Context-Aware Q&A: Answer questions based only on the provided textual context.

Grounded Responses: Ideal for research, ensuring factual accuracy and reducing hallucinations common in large language models.

Interactive Interface: Designed to run smoothly in Jupyter or Google Colab environments.

Rapid Analysis: Quickly extract key information or summaries from lengthy documents.

Prerequisites

Before running the notebook, you will need the following:

Python 3.8+

A Mistral API Key. You can obtain one from Google AI Studio.

Setup and Installation

1. Clone the Repository

Clone this repository to your local machine:

git clone <your-repo-link>
cd <your-repo-name>


2. Install Dependencies

Install the required Python libraries. This notebook relies on the official Google GenAI SDK and a few other standard data science libraries.

pip install google-genai ipywidgets pandas numpy


3. Set up Your API Key

For security and best practice, set your API key as an environment variable. In the first cell of the notebook, you will see instructions to load this key.

If running locally (e.g., in VS Code or terminal):

export MOSTRAL_API_KEY="YOUR_API_KEY_HERE"


If running in Google Colab or Jupyter:

You can run the following Python cell to set the key directly:

import os
os.environ['MISTRAL_API_KEY'] = 'YOUR_API_KEY_HERE'


Usage

Step 1: Open the Notebook

Open ResearchAssistant.ipynb in your preferred Jupyter environment (Jupyter Lab, Jupyter Notebook, or Google Colab).

Step 2: Run Cells Sequentially

Run each cell in the notebook. The workflow is generally as follows:

Setup Cell: Imports libraries and initializes the Mistral client.

Context Input Cell: This is where you paste or load your document/research material.

Prompting Cell: Input your question.

Generation Cell: This cell executes the model call, combining your context and your question to generate a grounded answer.

Example Interaction

The notebook's core function is to generate an answer based on a specific context.

Context Provided:

"Neural Additive Models (NAMs) are a class of interpretable neural networks. NAMs learn a linear combination of neural networks that each attend to a single input feature. These networks are trained jointly and can learn arbitrarily complex non-linear relationships..."

User Question:

What is a Neural Additive Model?

Generated Answer:

Neural Additive Models (NAMs) are a type of neural network architecture that allows for interpretable models while still maintaining high levels of accuracy. NAMs are based on the idea of additive models, which are a type of statistical model that can be decomposed into the sum of several simpler models. In NAMs, each neural network is trained to focus on a single input feature, and the final model is the sum of all of the neural networks.

Contributing

We welcome contributions to improve this research tool! Feel free to open issues or submit pull requests.
