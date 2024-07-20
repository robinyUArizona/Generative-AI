# LangChain-CrashCourse
### Problem Statement
AtliQ Tees is a T-shirt store where they maintain their inventory, sales and discounts data in MySQL database into 2 tables "t_shirts" and "discounts". A store manager will may ask questions such as,
- How many white color Adidas t shirts do we have left in the stock?
- How much sales our store will generate if we can sell all extra-small size t shirts after applying discounts?

![Alt text](https://github.com/robinyUArizona/Generative-AI/blob/main/Retail%20Industry%20LLM%20projects%20using%20LangChain%20Google%20Palm/AtliQ_T_shirts.jpg)

### Overview of the project
![Project Overview](https://github.com/robinyUArizona/Generative-AI/blob/main/Retail%20Industry%20LLM%20projects%20using%20LangChain%20Google%20Palm/Overview_project.jpg)

### Solution
Built an LLM system based on Google Palm (PaLM2) within the Langchain framework that could interact with a MySQL database using the SQLDatabaseChain class. Users could ask questions in natural language, and the system generated answers by converting those questions into SQL queries and then executing those queries on the MySQL database.

To address the occasional failure of Google Palm LLM models in handling complex queries, the few-shot learning technique was employed.

Few-shot learning involved preparing a training dataset with sample questions and corresponding SQL queries. These training datasets were converted into embedding vectors using Hugging Face and stored in a vector database (ChromaDB). This setup was then paired with Google Palm LLM using a few-shot prompt template to create the SQL Database Chain. Finally, the UI was built using Streamlit.

**Technologies**: MySQL, Hugging Face, ChromaDB, LangChain, Google Palm LLM model, Streamlit