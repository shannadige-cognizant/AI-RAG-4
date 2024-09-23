# Simple RAG Demo

Retrieval-Augmented Generation (RAG) is the process of optimizing the output of a large language model, so it references an authoritative knowledge base outside of its training data sources before generating a response.

This is a quick demonstration of RAG capabilities, we use it to showcase what retrieval within an unstructured database would look like for a given use case. This use case particularly is for a fictional airline company, but can be repurposed for any use case.

The application runs on pure Python and UI is presented via Streamlit.

![](https://holocron.so/uploads/5d2a95f5-screenshot-2024-09-23-at-2.52.53-pm.png)


## Use cases

We have identified the following use cases for RAG architecture to assist in conversational AI scenarios. More can be added in the future:

- Chat services in sales or customer support, using dynamically changing knowledge & contextual understanding  
- Personal assistants, providing personalization based on knowledge of the user
- Search engines, providing precise answers and speed of index searching

## Installation instructions

1. Required specs to get this running out of the box: MacOS machine, Python 3.10 or greater, Ollama and local LLM "llama3" installed. Some adjustments need to be made for other OS or LLM.
2. Clone this repo.
3. Create a virtual environment and install the necessary dependencies from requirements.txt

   ```plaintext
   python -m venv .
   source bin/activate
   
   pip install -r requirements.txt
   ```

   Some key libraries: langchain_community, ollama, streamlit
4. Run the app using `streamlit run app-dbair.py`

## Using the chatbot

- Uploading files to simulate the knowldge base, files are vectorized by langchain and temporarily stored in cache. 
- Conversation with bot triggered under chat history.
