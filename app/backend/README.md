# Backend for RAG Chat App with Azure OpenAI and Azure AI Search

This directory contains the backend code for the RAG Chat App, which integrates Azure OpenAI and Azure AI Search to provide a chat interface over custom data.

## Table of Contents

- [Overview](#overview)
- [Setup](#setup)
- [Configuration](#configuration)
- [Running the Backend](#running-the-backend)
- [API Endpoints](#api-endpoints)
- [File Structure](#file-structure)

## Overview

The backend is built using [Quart](https://quart.palletsprojects.com/), a Python framework for asynchronous web applications. It handles document processing, user authentication, and communication with Azure services.

## Setup

1. **Create a Python virtual environment:**

    ```sh
    python3 -m venv .venv
    ```

2. **Activate the virtual environment:**

    - On Windows:

        ```sh
        .venv\Scripts\activate
        ```

    - On macOS/Linux:

        ```sh
        source .venv/bin/activate
        ```

3. **Install the required packages:**

    ```sh
    pip install -r requirements.txt
    ```

## Configuration

The backend requires several environment variables to be set for Azure services and other configurations. These can be set in a `.env` file or directly in the environment.

## Running the Backend

To start the backend server, run:

```sh
../../.venv/bin/python -m quart --app main:app run --port 50505 --host localhost --reload
```

## API Endpoints

The backend exposes several API endpoints for document processing and user interactions. Here are some key endpoints:

- **Upload Document:**
    - `POST /upload`
    - Authenticated endpoint to upload documents.

- **Delete Uploaded Document:**
    - `POST /delete_uploaded`
    - Authenticated endpoint to delete uploaded documents.

## File Structure

- `app.py`: Main application file that initializes the Quart app and defines routes.
- `prepdocs.py`: Contains functions for preparing and processing documents.
- `requirements.txt`: Lists the Python dependencies for the backend.
- `config.py`: Configuration settings for the backend.
- `utils/`: Utility functions and helpers.

## Additional Documentation

For more details on deploying and customizing the backend, refer to the main [README](../../README.md) and the [docs](../../docs) folder.
