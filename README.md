#### Setup
1. Installation
  `pip install -r requirements.txt`

2. Add pdf's
  Add the pdfs you want to delete or upload to pinecone in "docs".
  Remove them after you executed the program.

3. Add your api-keys in config.py and set the environments
  Modify the following code block in "loading.py" and "delete.py"
  ```python
    embeddings = OpenAIEmbeddings(openai_api_key="", model="text-embedding-ada-002")
    pinecone.init(api_key="", environment="")
    index = ""
    index = pinecone.Index(index)
    namespace=""
  ```

#### Upload to pinecone
`python loading.py`

#### Delete from pinecone
`python delete.py`