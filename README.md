# CLIP Image-Search-Engine

## Project Overview

This project leverages OpenAI's CLIP (Contrastive Language-Image Pretraining) model to develop an image search engine. By utilizing CLIP's ability to encode both text and images into a shared latent space, the model allows for efficient matching of natural language queries with images. The Unsplash dataset, containing nearly 2 million photos, was used as the source of images.

## Features

- **Text-to-Image Search**: Users can input natural language descriptions to search for the best-matching images.
- **Efficient Image Retrieval**: Pre-computed feature vectors of the entire Unsplash dataset enable fast and efficient image lookups.
- **CLIP Integration**: Uses OpenAI’s CLIP model to generate embeddings for both text queries and images.

## Dataset

- **Unsplash Dataset**: The project uses the complete Unsplash dataset, which contains approximately 2 million images, pre-processed with CLIP to create feature vectors.

## Project Structure

- `data/`: Contains pre-computed CLIP embeddings for all images in the dataset.
- `models/`: Stores the CLIP model and related utilities for loading and processing images/text.
- `search_engine.py`: Core functionality of the search engine, including loading embeddings and performing similarity searches.
- `app.py`: A basic web interface for interacting with the search engine.
- `README.md`: Project documentation.

## How It Works

1. **Image Embeddings**: Each image in the Unsplash dataset is processed through CLIP to generate a high-dimensional feature vector.
2. **Text Embeddings**: When a user inputs a search query, CLIP converts the text into a feature vector within the same latent space.
3. **Similarity Matching**: The system computes cosine similarity between the text embedding and the pre-computed image embeddings to return the best matches.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/username/image-search.git
    cd project-name
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the application:
    ```bash
    python app.py
    ```

## Usage

- Launch the application and enter a natural language description in the search box to find relevant images from the Unsplash dataset.

## Technologies Used

- **OpenAI CLIP**: For generating embeddings of both images and text.
- **Python**: Core programming language used for processing and server-side logic.
- **Flask**: For building the web interface (optional, if a web app is included).
- **Unsplash Dataset**: Source of images for the project.
