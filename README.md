# My First SmolAgent

A beginner-friendly project exploring the smolagents framework with a local language model running in Google Colab.

This project demonstrates how to set up smolagents, verify GPU availability, load a local Qwen instruction-following model using TransformersModel, and generate a response from a user prompt.

## Project Overview

The notebook was developed and tested in Google Colab with an NVIDIA Tesla T4 GPU.

The project uses:

* Python
* Hugging Face smolagents
* Hugging Face Transformers
* PyTorch
* Qwen/Qwen2.5-1.5B-Instruct
* Google Colab GPU

The main purpose of the project is to understand the basic setup required to run a local language model through the smolagents framework.

## Architecture

text
Google Colab
     |
     v
NVIDIA Tesla T4 GPU
     |
     v
Install smolagents + Transformers + Accelerate
     |
     v
Initialize TransformersModel
     |
     v
Qwen/Qwen2.5-1.5B-Instruct
     |
     v
User Prompt
     |
     v
Local Model Inference
     |
     v
Generated Response

## How It Works

The notebook follows these steps:

1. Checks the available NVIDIA GPU using nvidia-smi.
2. Installs or updates smolagents, Transformers, and Accelerate.
3. Verifies the installed smolagents version.
4. Imports the required smolagents components.
5. Checks the PyTorch version and confirms CUDA availability.
6. Loads Qwen/Qwen2.5-1.5B-Instruct through smolagents.TransformersModel.
7. Sends a user prompt to the local model.
8. Prints the generated response.

## Model

The project uses:

Qwen/Qwen2.5-1.5B-Instruct

The model is loaded with:

python
from smolagents import TransformersModel

model = TransformersModel(
    model_id="Qwen/Qwen2.5-1.5B-Instruct",
    device_map="auto"
)


The device_map="auto" setting allows the Transformers-based model loading process to automatically determine an appropriate device placement.

## Hardware Environment

The notebook successfully detected:

* GPU: NVIDIA Tesla T4
* GPU memory: 15 GB
* PyTorch: 2.11.0+cu128
* CUDA available: True
* smolagents: 1.26.0

The model download shown in the notebook includes approximately 3.09 GB of model weights.

## Example

The notebook sends the following prompt to the model:

text
What is the capital of India?


The recorded output is:

text
The capital of India is New Delhi.


## Installation

Run the following command in Google Colab:

bash
!pip install -U "smolagents[transformers]" transformers accelerate


Then verify the installation:

python
import smolagents

print("smolagents version:", smolagents.__version__)


## Project Structure

text
My_First_SmolAgent.ipynb
README.md


The main implementation is contained in the Jupyter notebook.

## Important Scope

This project is intentionally simple and focuses on local model inference through smolagents.

The current notebook:

* Loads a local Qwen model.
* Accepts a text prompt.
* Generates a text response.
* Uses the Google Colab GPU for model execution.

The current notebook does *not*:

* Create a CodeAgent instance.
* Execute agent steps.
* Use DuckDuckGoSearchTool.
* Perform web searches.
* Connect to an external inference API.
* Implement custom tools.

CodeAgent and DuckDuckGoSearchTool are imported in the notebook, but they are not used in the executed model workflow.

## Learning Outcome

This project provides a basic understanding of:

* Setting up smolagents in Google Colab.
* Checking GPU and CUDA availability.
* Loading a local instruction-following model.
* Using TransformersModel from smolagents.
* Sending a structured chat message to a local model.
* Receiving and displaying the model's generated response.

## Future Extension

A natural next step would be to build an actual tool-using agent with CodeAgent and one or more tools. That would extend this basic local model setup into a more complete agent workflow.

## Project Status

Completed as a first hands-on experiment with smolagents and local language model inference in Google Colab.
