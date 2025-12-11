# Info
This is RAG connected to fine-tuned SLMs. Answers questions based on loaded files. 
Ready to use, by contains only 20 test application loaded to save disk space.

# Requirements 

pip install unsloth
pip install chromadb
pip install langchain_text_splitters
pip install sentence_transformers
...
and others

# Files

slm_rag.py - main file
promt.txt - contains promts for slms, each line connected to the same line in questions.txt
application_list.txt - list of application that are present in the ChromaDB storage. Nesesary to extract correct context for a question from db.
questions.txt - list of questions we a using to evaluate slms. 

# Usage

terminal: slm_rag.py -init # creating embeding vectors from ./storage_test. Don't forget to clear content of ./chroma_store before using. You don't need this command by default.

terminal: slm_rag.py -multi -m "gemma" # many requests (from questions.txt) about applications (application_list.txt) to gemma using promt (promt.txt)
terminal: slm_rag.py -multi -m "phi" # many requests (from questions.txt) about applications (application_list.txt) to phi using promt (promt.txt)

# Settings

To configure script change global vars inside script
