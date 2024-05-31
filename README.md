## README

# SAM Project

Welcome to the SAM Project! This repository contains a Jupyter Notebook implementation of the SAM (Semantic Answer Machine) model. The purpose of this project is to generate responses to user queries based on the content of a provided document, much like a chatbot. Additionally, the SAM model can identify the most relevant page within the document that corresponds to the user's query and display it.

## Features

- **Query-Based Response Generation**: The SAM model processes user queries and generates responses specific to the content of the provided document.
- **Page Relevance Identification**: The model identifies and highlights the exact page within the document that is most relevant to the user's query.

## Installation

To get started with the SAM Project, follow these steps:

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/sam-project.git
    cd sam-project
    ```

2. **Install the required dependencies**:
    If you are running the project in Google Colab, the dependencies will be installed automatically. Otherwise, you can install the dependencies manually:

    ```sh
    pip install -U torch
    pip install PyMuPDF
    pip install tqdm
    pip install sentence-transformers
    pip install accelerate
    pip install bitsandbytes
    pip install flash-attn --no-build-isolation
    ```

## Dependencies

The following dependencies are required for the SAM Project:

- `torch` (requires version 2.1.1+ for efficient sdpa implementation)
- `PyMuPDF` (for reading PDFs with Python)
- `tqdm` (for progress bars)
- `sentence-transformers` (for embedding models)
- `accelerate` (for quantization model loading)
- `bitsandbytes` (for quantizing models to save storage space)
- `flash-attn` (for faster attention mechanism, leading to faster LLM inference)

In Google Colab, these dependencies can be installed using the following commands:

```python
import os

if "COLAB_GPU" in os.environ:
    print("[INFO] Running in Google Colab, installing requirements.")
    !pip install -U torch
    !pip install PyMuPDF
    !pip install tqdm
    !pip install sentence-transformers
    !pip install accelerate
    !pip install bitsandbytes
    !pip install flash-attn --no-build-isolation
```

## Usage

1. **Open the Jupyter Notebook**:
    ```sh
    jupyter notebook
    ```
2. **Navigate to the `SAM_Project.ipynb` file** and open it.

3. **Run the Notebook**: Follow the instructions within the notebook cells to load the document, input queries, and view the responses generated by the SAM model.

## Functions

### 1. `generate_response(query, document)`
Generates a response to the given query based on the content of the provided document.

- **Parameters**:
  - `query` (str): The user's query.
  - `document` (str): The content of the document.

- **Returns**:
  - `response` (str): The generated response.

### 2. `find_relevant_page(query, document)`
Identifies the page within the document that is most relevant to the given query.

- **Parameters**:
  - `query` (str): The user's query.
  - `document` (str): The content of the document.

- **Returns**:
  - `page_number` (int): The number of the page that is most relevant to the query.
  - `page_content` (str): The content of the most relevant page.



## Contact

For any questions or suggestions, please contact [riteshkantule@gmail.com](mailto:riteshkantule@gmail.com).

---

Thank you for using the SAM Project! We hope you find it useful and informative.
