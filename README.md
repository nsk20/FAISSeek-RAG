# FAISSeek-RAG
## RAG Model with Deepseek-r1 and FAISS

This project demonstrates how to create a Retrieval-Augmented Generation (RAG) model using the Deepseek-r1 language model and FAISS for vector similarity search. The model is exposed via a public API using ngrok.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/nsk20/RAG_Model.git
   cd RAG_Model

2.**Install the required dependencies:**
	i. Visit https://ollama.com/ and follow the instructions to download Ollama in your PC and then ```bash ollama run deepseek-r1:1.5b 
	ii. Visit https://dashboard.ngrok.com/ and follow the instructions to download Ngrok in your PC and then ```bash ngrok http --host-header=rewrite localhost:11434
	iii. After Running the Ngrok cmd in the Terminal use will see an API endpoint ending with: ".ngrok-free.app/"
	iv. Keep Both Ollama and Ngrok running untill the end of the project. 


## Usage

1. You can use the provided python Notebook in the GIT and upload it to Google Colab or other similar software.
2. Find the ngrok_url variable in the notebook and replace with your own API endpoint that running in the background.
3. After running the file it will ask to upload a .txt file in the Console. Upload somefile(Start trying with small files and then gradually increase the size of the file depending the GPU, CPU & RAM of your PC).
4. Enter your questions in the console. The model will retrieve relevant context from the documents and generate an answer using the Deepseek-r1 model.

## Project Structure

- **main.py:** Main script containing the RAG model implementation.
- **requirements.txt:** List of Python dependencies.
- **README.md:** Project documentation.


## Dependencies
- **transformers:** For tokenization and model loading.
- **torch:** For tensor operations.
- **faiss:** For vector similarity search.
- **requests:** For making HTTP requests to the ngrok API.
- **google.colab:** For file uploads in Google Colab.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request.

#### **LICENSE**

MIT License

Copyright (c) 2025 Shyam Kumar

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
