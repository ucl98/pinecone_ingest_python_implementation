#### Setup
1. Installation:
  `pip install -r requirements.txt`

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
`python loading.py`

#### Delete from pinecone
`python delete.py`
