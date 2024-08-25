# Ed-Tech Company QA Assistant
This project is a QA (Question-Answering) assistant designed for an Ed-Tech company. It leverages vector databases, state-of-the-art language models, and custom document embeddings to provide accurate responses to user queries based on a pre-defined knowledge base.

## Table of Contents
- [Features](#Features)
- [Installation](#Installation)
- [Usage](#Usage)
- [Project Structure](#ProjectStructure)
- [Future Enhancements](#FutureEnhancements)
- [Contributing](#Contributing)
- [License](#License)

## Features
- **Vector Database**: Utilizes FAISS for efficient similarity search across the knowledge base.
- **Custom Embeddings**: Powered by HuggingFaceEmbeddings using the sentence-transformers/all-MiniLM-L6-v2 model.
- **Large Language Model (LLM)**: Integrates Groq's LLaMA3 model (llama3-8b-8192) for generating context-aware responses.
- **CSV Loader**: Loads FAQs or other structured data from CSV files to populate the knowledge base.
- **Streamlit Interface**: A simple and interactive UI for asking questions and receiving answers.

## Installation
1. Clone the Repository:

```python
git clone https://github.com/shaadclt/Ed-Tech-Company-QA-Assistant.git
cd Ed-Tech-Company-QA-Assistant
```

2. Set Up a Virtual Environment:

```python
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

3. Install Dependencies:

```python
pip install -r requirements.txt
```

4. Environment Variables: Create a .env file in the project root and add your Groq API key:

```python
GROQ_API_KEY=your_groq_api_key_here
```

## Usage
1. Run the Streamlit App

```python
streamlit run main.py
```

2. Create the Knowledge Base:
To create the knowledge base from a CSV file, click the button Create Knowledgebase

3. Ask a Question: 
Enter a question in the Streamlit interface, and the assistant will provide a contextually accurate response based on the loaded knowledge base.

## Project Structure
- **langchain_helper.py**: Contains the logic for loading data, creating the vector database, and generating responses.
- **main.py**: The Streamlit application file.
- **faqs.csv**: A sample CSV file used to populate the knowledge base.
- **requirements.txt**: Lists all required Python packages.
- **.env**: Stores environment variables like API keys (not included in the repository for security reasons).
  
## Future Enhancements
- Expand Knowledge Base: Add more documents or data sources.
- Fine-Tune Models: Adjust the embeddings or LLM for more accurate responses.
- Advanced UI: Improve the Streamlit interface with additional features like response filtering or feedback mechanisms.

## Contributing
Feel free to fork this repository, create a feature branch, and submit a pull request for any enhancements or bug fixes.

## License
This project is licensed under the MIT License. See the [License](/LICENSE.txt) file for details.
