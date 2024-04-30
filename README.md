# Text Analytics API with FastAPI, Docker, and Hugging Face Transformers

Welcome to the Text Analytics API repository! This project provides a robust and scalable RESTful API for text classification tasks using FastAPI, Docker, and Hugging Face Transformers. With this API, you can easily perform sentiment analysis, emotion classification, and more on textual data. Let's dive into the details!

# Overview

Our primary goal with this project is to empower developers and data scientists with an efficient tool for text analysis. By leveraging FastAPI, Docker, and Hugging Face Transformers, we've created an API that delivers real-time insights into textual data, enabling users to make informed decisions based on sentiment and emotion analysis.

# Dependencies
To run this project, you'll need the following dependencies:

**FastAPI**: A cutting-edge web framework for building APIs with Python, known for its speed and ease of use.

**Transformers**: The Hugging Face library, offering a wide range of pre-trained models for natural language processing (NLP) tasks.

**Pyngrok**: A Python wrapper for ngrok, facilitating the exposure of local servers over public URLs for easy testing and sharing.

**Nest_asyncio**: A library enabling nested asyncio event loops, crucial for running asyncio within other asyncio loops seamlessly.

**NLTK**: The Natural Language Toolkit, providing tools and resources for text processing and analysis tasks.

**Pydantic**: A data validation library for Python, ensuring robustness and reliability in handling API input and output.

# Code Explanation
Here's a breakdown of the main components of our code:

**main.py**: This file houses the core functionality of our FastAPI application, including endpoint definitions, request and response models, and model integration for text classification.

**test.py**: Here, you'll find unit tests for our API endpoints, implemented using FastAPI's TestClient to ensure the reliability and correctness of our API.

**Dockerfile**: Our Dockerfile specifies the environment and instructions for building the Docker image for our FastAPI application, streamlining deployment and portability.

**requirements.txt**: This file lists all the Python dependencies required by our project, making it easy to install and manage dependencies.

# FastAPI Integration
Our API leverages FastAPI to provide a RESTful interface with the following endpoints:

**GET /**: A welcome endpoint that redirects users to the Swagger UI page, providing interactive documentation and exploration capabilities.
**POST /analyze/**: The primary endpoint for text classification tasks, accepting JSON input with a text field and returning sentiment/emotion analysis results in real-time.

# Dockerization
We've containerized our API using Docker for seamless deployment across different environments. Our Dockerfile specifies the environment and instructions for building the Docker image, ensuring consistency and ease of deployment.

# Hugging Face Model Details
Our API utilizes the bert-base-uncased model from the Hugging Face model hub. This model is a fine-tuned version of BERT for general-purpose text classification tasks, offering excellent performance and accuracy across various domains.

# Hugging Face Space Link
You can access the trained model and associated resources on our Hugging Face Space:[ Text-classification-fast API](https://huggingface.co/spaces/emanism6/Text-Classification-Fastapi)

# Building and Running the Container
To build and run the Docker container, follow these simple steps:

1. Ensure Docker is installed on your system.
2. Clone this repository to your local machine.
3. Navigate to the project directory in your terminal.
4. Build the Docker image using the following command:

**Copy code**
docker build -t text-analytics-api .
### Once the image is successfully built, run the container with the following command:

**Copy code**
docker run -d -p 8000:8000 text-analytics-api:latest
Voila! Your API is now up and running at http://localhost:8000.

# Interacting with the API
You can interact with our API using various tools, such as cURL, Postman, or by programing HTTP requests. Additionally, you can utilize the Swagger UI provided by FastAPI for easy testing and exploration:

1.  Open your web browser and navigate to http://localhost:8000/.
2.  Explore the Swagger UI interface to discover and interact with the API endpoints.
3.  Click on the /analyze/ endpoint, then click on "Try it out" to input your text data.
4.  After entering the text data, click on "Execute" to send the request and view the sentiment/emotion analysis results.
5.  
Feel free to explore the code and documentation to better understand how our API works and how you can leverage it for your text classification needs. If you have any questions or feedback, don't hesitate to reach out!

