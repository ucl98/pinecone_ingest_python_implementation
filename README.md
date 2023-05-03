#### Setup
1. Installation
  `pip install -r requirements.txt`

2. Add your api-keys in config.py and set the environments
  Modify the following code block in "config.py"
  ```python
OPENAI_API_KEY = "your_openai_api_key"
PINECONE_API_KEY = "your_pinecone_api_key"
PINECONE_INDEX_NAME = "your_pinecone_index_name"
PINECONE_NAMESPACE = "your_pinecone_namespace"
  ```

3. Add pdf's
  Create a new folder "docs" inside the project.
  Add the pdfs you want to delete or upload to pinecone in "docs".
  Remove them after you executed the program.

#### Upload to pinecone
`python loading.py`

#### Delete from pinecone
`python delete.py`
