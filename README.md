# FastAPI Sentiment Analysis and Text Summarization API

This repository contains code to create a simple API using FastAPI for performing sentiment analysis, text summarization, and emotion classification using pre-trained models from the Hugging Face Transformers library.

## Introduction

FastAPI is a modern, fast (high-performance) web framework for building APIs with Python 3.6+ based on standard Python type hints. This project demonstrates how to create API endpoints for sentiment analysis, text summarization, and emotion classification using FastAPI.

## Features

- **Sentiment Analysis:** Classifies the sentiment of the input text as positive, negative, or neutral.
- **Text Summarization:** Summarizes long pieces of text into concise summaries.
- **Emotion Classification:** Identifies the emotion behind the summarized text.
- **Custom LLM Endpoint:** Example of integrating OpenAI's GPT-4 for custom language model responses.

## Installation

To install the required dependencies, run:

```bash
pip install fastapi nest-asyncio pyngrok uvicorn transformers openai
```

## Usage

1. **Run the FastAPI server:**
   - The server runs on `http://localhost:8000` by default.
   - Use `ngrok` to expose the server to the internet for public access.

2. **Using the API:**
   - After running the server, you can access the API endpoints to perform sentiment analysis, text summarization, emotion classification, and more.

## API Endpoints

### Home

- **URL:** `/`
- **Method:** `GET`
- **Description:** Returns a welcome message.

### Sentiment Analysis

- **URL:** `/sentiment/{input_text}`
- **Method:** `GET`
- **Description:** Returns the sentiment analysis of the provided input text.

### Text Summarization and Emotion Classification

- **URL:** `/ai/{input_text}`
- **Method:** `GET`
- **Description:** Summarizes the input text and then classifies the emotion of the summarized text.

### Custom LLM Endpoint

- **URL:** `/chat/{prompt}`
- **Method:** `GET`
- **Description:** Uses OpenAI's GPT-4 to generate a response based on the provided prompt.

## Running on Google Colab

This code can be executed in a Google Colab environment. Here's a brief overview:

- **Installing Dependencies:** Colab requires installing FastAPI, `nest-asyncio`, `pyngrok`, and `uvicorn`.
- **Running the Server:** The server is run using `uvicorn`, and `ngrok` is used to expose it to the public.
- **Custom API Integration:** The code demonstrates how to use pre-trained models for NLP tasks and integrate a custom LLM using OpenAI's API.

Certainly! Here’s how you can test the endpoints using Postman and directly through `cURL`.

### Example Usage

#### Home Endpoint

**URL:** `/`

- **Method:** `GET`
- **Postman:** 
  - Set the request type to `GET`.
  - Enter the URL provided by `ngrok` (e.g., `https://<your-ngrok-url>/`).
  - Click on `Send`.

- **cURL:**
  ```bash
  curl -X GET "https://<your-ngrok-url>/"
  ```

#### Test Endpoint

**URL:** `/test`

- **Method:** `GET`
- **Postman:** 
  - Set the request type to `GET`.
  - Enter the URL provided by `ngrok` (e.g., `https://<your-ngrok-url>/test`).
  - Click on `Send`.

- **cURL:**
  ```bash
  curl -X GET "https://<your-ngrok-url>/test"
  ```

#### Sentiment Analysis

**URL:** `/sentiment/{user_input}`

- **Method:** `GET`
- **Example Input:** `I love FastAPI`

- **Postman:**
  - Set the request type to `GET`.
  - Enter the URL: `https://<your-ngrok-url>/sentiment/I%20love%20FastAPI`
  - Click on `Send`.

- **cURL:**
  ```bash
  curl -X GET "https://<your-ngrok-url>/sentiment/I%20love%20FastAPI"
  ```

#### Text Summarization & Emotion Classification

**URL:** `/ai/{input_text}`

- **Method:** `GET`
- **Example Input:** `FastAPI is a modern, fast (high-performance) web framework for building APIs with Python 3.6+ based on standard Python type hints.`

- **Postman:**
  - Set the request type to `GET`.
  - Enter the URL: `https://<your-ngrok-url>/ai/FastAPI%20is%20a%20modern,%20fast%20(high-performance)%20web%20framework%20for%20building%20APIs%20with%20Python%203.6+%20based%20on%20standard%20Python%20type%20hints.`
  - Click on `Send`.

- **cURL:**
  ```bash
  curl -X GET "https://<your-ngrok-url>/ai/FastAPI%20is%20a%20modern,%20fast%20(high-performance)%20web%20framework%20for%20building%20APIs%20with%20Python%203.6+%20based%20on%20standard%20Python%20type%20hints."
  ```

#### Custom GPT-3/4 Response

**URL:** `/gpt/{prompt}`

- **Method:** `GET`
- **Example Prompt:** `Tell me a joke.`

- **Postman:**
  - Set the request type to `GET`.
  - Enter the URL: `https://<your-ngrok-url>/gpt/Tell%20me%20a%20joke.`
  - Click on `Send`.

- **cURL:**
  ```bash
  curl -X GET "https://<your-ngrok-url>/gpt/Tell%20me%20a%20joke."
  ```

#### Multiplication Table

**URL:** `/{number}`

- **Method:** `GET`
- **Example Input:** `5`

- **Postman:**
  - Set the request type to `GET`.
  - Enter the URL: `https://<your-ngrok-url>/5`
  - Click on `Send`.

- **cURL:**
  ```bash
  curl -X GET "https://<your-ngrok-url>/5"
  ```

Replace `<your-ngrok-url>` with the actual `ngrok` URL provided when you start your FastAPI server.


