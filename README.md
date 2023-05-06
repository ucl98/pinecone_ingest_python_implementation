#### My specs
- OS: macOS Ventura 
- Python: 3.11.2
  - https://www.python.org/downloads/release/python-3112/

#### Setup
0. Forewords:
  This project is not part of gpt4-pdf-chatbot-langchain. Both projects should not be combined.
  However, when you use this project to ingest your files, you will still see them in the chatbot of gpt4-pdf-chatbot-langchain IF the pinecone index and the namespaces in both projects are the same.

  ![image](https://user-images.githubusercontent.com/132441647/236612075-22b00aaf-ffe9-4de7-b0a2-5e59bb209931.png)

1. Installation:
  - Option 1: pip install:
    Type `pip install -r requirements.txt` in the project's terminal.   
  
  - Option 2: If that is not working, install the dependencies one by one: 
    Install the following depencencies at the projects terminal
    `pip install langchain`
    `pip install pinecone-client`
    `pip install pypdf`

2. Modify the following code block in "config.py".
  ```python
OPENAI_API_KEY = "your_OPENAI_API_KEY"
PINECONE_API_KEY = "your_PINECONE_API_KEY"
PINECONE_ENVIRONMENT = "your_PINECONE_ENVIRONMENT"
PINECONE_INDEX_NAME = "your_PINECONE_INDEX_NAME"
PINECONE_NAMESPACE = "pdfs"
  ```

3. Create a new folder "docs" inside the project.
  Add the pdfs you want to delete or upload to pinecone in "docs".
  Remove them after you ingested or delete them.

#### Upload to pinecone
`python ingest.py`

#### Delete from pinecone
`python delete.py`

#### Was the ingest successful?
To check wether or not the ingest process was successful, go to pinecone and see if vectors where added in the namespace you defined.
- If my program throws no error, it is safe to assume that everything was correct.

![image](https://user-images.githubusercontent.com/132441647/236612380-9ee52077-aa5f-4f7d-bd61-a606f4bbc5ce.png)
