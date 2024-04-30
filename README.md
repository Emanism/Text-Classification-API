# Text Classification API with FastAPI, Docker, and Hugging Face Transformers

This repository contains code for building a RESTful API using FastAPI to perform text classification (sentiment analysis, emotion classification, etc) using a pre-trained Hugging Face Transformer model. The API is containerized using Docker for easy deployment.


## Overview

The main objective of this project is to develop a robust and scalable API for text classification tasks using FastAPI, Docker, and Hugging Face Transformers. The API allows users to submit text data and receive sentiment or emotion analysis results in real time.

---

## Prerequisites and Dependencies

The project relies on the following dependencies:

- **FastAPI:** A modern web framework for building APIs with Python.
- **Transformers:** The Hugging Face library for natural language processing (NLP) tasks, including pre-trained models.
- **Pyngrok:** A Python wrapper for ngrok, which exposes local servers over public URLs.
- **Nest_asyncio:** A library for running asyncio nested in other asyncio loops.
- **NLTK:** The Natural Language Toolkit for text processing tasks.
- **Pydantic:** A data validation library for Python.

---

## Codebase

The main components of the code include:

- **main.py:** This file contains the FastAPI application, including the definition of endpoints, request and response models, and model integration.
- **test.py:** This file contains unit tests for the API endpoints using FastAPI's TestClient.
- **Dockerfile:** The Dockerfile defines the environment and instructions for building the Docker image for the FastAPI application.
- **requirements.txt:** This file lists all the Python dependencies required by the project.

---

## FastAPI Integration Essentials

FastAPI is used to develop the RESTful API with the following endpoints:

- **GET /:** A welcome endpoint that redirects to the Swagger UI page.
- **POST /analyze/:** The main endpoint for text classification. It accepts JSON input with a text field and returns the sentiment/emotion analysis results.

---

## Containerization with Docker

The project is containerized using Docker for easy deployment. The Dockerfile defines the environment and instructions for building the Docker image, including installing dependencies and running the FastAPI application.

---

## Hugging Face Model 

The API utilizes the `distilbert-base-multilingual-cased-sentiments-student` model from the Hugging Face model hub. This model is a distilled version of the DistilBERT model trained for sentiment analysis tasks across multiple languages.

---

## Hugging Face Space Link

The trained model and associated resources are hosted on the following Hugging Face Space: https://huggingface.co/spaces/emanism6/Text-Classification-Fastapi

---


## Containerization: Building and Deployment
To initiate the construction and deployment of the Docker container, adhere to the subsequent steps:

**Confirm Docker Installation**: Verify that Docker is installed on your system to proceed with containerization seamlessly.

**Repository Cloning**: Clone the repository to your local machine, ensuring access to the essential files and configurations required for container creation.

**Directory Navigation**: Navigate to the project directory within your terminal environment, facilitating easy access to project resources and files necessary for containerization.

**Build Docker Image**: Execute the following command in your terminal to initiate the Docker image's construction, incorporating dependencies and configurations defined within the Dockerfile:

```
docker build -t fastapi-test-sentiment-api-0.1.2 .
```

5. Once the image is built successfully, run the container with the following command:

```
docker run -d -p 8000:8000 fastapi-test-sentiment-api-0.1.2:latest
```

6. The API will now be accessible at `http://localhost:8000`.

---

## Interacting with the API

You can interact with the API using tools like cURL, Postman, or by sending HTTP requests programmatically. Alternatively, you can use the Swagger UI provided by FastAPI for easy testing and exploration.

1. Open your web browser and navigate to `http://localhost:8000/`.
2. This will open the Swagger UI interface, where you can explore the API endpoints and submit requests with sample data.
3. Click on the `/analyze/` endpoint, and then click on "Try it out" to input your text data.
4. After entering the text data, click on "Execute" to send the request and view the response, which will include the sentiment/emotion analysis results.

---

Feel free to explore the code and documentation for more details on how the API works and how to interact with it.


