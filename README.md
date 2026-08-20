# 🤖 My First SmolAgent

A beginner-friendly project exploring **Hugging Face smolagents** and local LLM inference in Google Colab.

This project is part of my learning journey through the **Hugging Face Agents Course – Unit 1**.

## 🚀 Project Overview

In this project, I set up a local language model using Hugging Face's `smolagents` framework and tested it in Google Colab with a T4 GPU.

The project currently demonstrates:

* Installing `smolagents`
* Checking the installed package version
* Checking GPU availability
* Loading a local language model
* Using `TransformersModel`
* Sending a prompt to the model
* Generating a response

## 🛠️ Technologies Used

* Python
* Google Colab
* Hugging Face `smolagents`
* Hugging Face Transformers
* Qwen/Qwen2.5-1.5B-Instruct
* PyTorch
* NVIDIA T4 GPU

## 🤖 Model

**Qwen/Qwen2.5-1.5B-Instruct**

The model is loaded locally in Google Colab using `TransformersModel`.

## 📂 Project Structure

```text
My_First_SmolAgent/
│
└── My_First_SmolAgent.ipynb
```

## ▶️ How to Run

1. Open the notebook in Google Colab.
2. Enable a GPU runtime.
3. Install the required packages.
4. Load the Qwen model.
5. Run the model test.
6. Enter prompts and observe the generated responses.

## 💡 Example

Input:

```text
What is the capital of India?
```

Output:

```text
The capital of India is New Delhi.
```

## 📚 Learning Goal

The goal of this project is to understand the fundamentals of AI agents using Hugging Face `smolagents`, including:

* Models
* Agents
* Tools
* Agent reasoning
* Actions
* Observations

## 🔨 Next Step

The next version of this project will extend the model into a proper `CodeAgent` and add tools so that the agent can perform actions instead of only generating direct model responses.

## 👩‍💻 Author

Ishwarya

This is my first hands-on project while learning AI agents with Hugging Face `smolagents`.
