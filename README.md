# Project Description

## Research Paper Query Assistant with Streamlit and LangChain

This project provides a powerful, interactive application for querying and retrieving answers from research papers. Built with **Streamlit**, it leverages **LangChain** and advanced embedding models to process research papers, create vectorized embeddings, and deliver accurate answers to user queries.

---

### Features
1. **Document Loading and Parsing**:
   - Automatically loads PDF research papers from the `research_papers` directory.
   - Splits documents into smaller, overlapping chunks for efficient processing using `RecursiveCharacterTextSplitter`.

2. **Vector Embedding Creation**:
   - Uses **OllamaEmbeddings** to generate high-quality embeddings for document chunks.
   - Stores the embeddings in a **FAISS** vector database for fast retrieval.

3. **Contextual Query Answering**:
   - Powered by the **LangChain** framework and **ChatGroq (Llama3-8b-8192)** for natural language understanding.
   - Combines document context with user queries to generate accurate, context-aware answers.

4. **Interactive UI with Streamlit**:
   - User-friendly interface to input queries and trigger document embedding creation.
   - Real-time feedback on embedding creation and query results.

---

### Workflow
1. **Document Embedding**:
   - Load PDFs from the `research_papers` directory.
   - Split documents into manageable chunks.
   - Generate vector embeddings for document chunks and store them in the FAISS vector store.

2. **Querying**:
   - Enter a question or query into the provided text box.
   - The system retrieves the most relevant document chunks and generates a contextually accurate answer using the `ChatGroq` LLM.

---

### Requirements
- **Python 3.9+**
- **Packages**:
  - `streamlit`
  - `langchain_groq`
  - `langchain_community`
  - `langchain`
  - `faiss`
  - `dotenv`

---

### How to Run
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your_username/your_repo_name.git
   cd your_repo_name
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up Environment Variables**:
   - Add your `GROQ_API_KEY` to a `.env` file:
     ```
     GROQ_API_KEY=your_api_key_here
     ```

4. **Run the Streamlit App**:
   ```bash
   streamlit run app.py
   ```

5. **Upload Research Papers**:
   - Place your PDF files in the `research_papers` directory.

6. **Query the Research Papers**:
   - Enter your query in the text box and retrieve the context-aware answer.

---

### Future Enhancements
- Add support for additional document types (e.g., Word, TXT).
- Improve UI/UX for displaying answers and retrieved document context.
- Enhance scalability by integrating with cloud-based vector databases.

---

Feel free to explore, contribute, and provide feedback! 😊
