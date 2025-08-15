# CsvPal-AI
<img width="1112" height="480" alt="Screenshot 2025-08-15 162809" src="https://github.com/user-attachments/assets/1cd3aca4-c320-486a-aaab-573a6361134a" />

**CsvPal-AI** is a Retrieval-Augmented Generation (RAG) powered assistant that allows you to interactively analyze your CSV data using natural language queries. Upload any CSV file, ask questions about your data, and receive answers *grounded strictly in your file*—complete with ready-to-run Python (pandas) code snippets to reproduce the result.

---

## 🚀 Features

- **Chat with Your CSV:** Upload a CSV file, ask questions in plain English, and receive clear, data-driven answers.
- **RAG-Powered Q&A:** The assistant retrieves the top-10 most relevant rows (or data chunks) from your CSV for each question, ensuring answers are based on actual data.
- **Python Code Generation:** Each answer includes executable pandas code using the loaded DataFrame (`df`) so you can replicate the analysis yourself.
- **No Hallucination:** If the answer can't be found in your data, the assistant will say so—no guessing or invented information.
- **User-Friendly Web UI:** Built with Gradio, featuring file upload, data preview, and interactive Q&A.

---

## 🏗️ How It Works

1. **Upload:** Select and upload your CSV file through the web interface.
2. **Indexing:** The app uses sentence-transformer embeddings to index your data for fast, semantic retrieval.
3. **Ask:** Enter your question (e.g., "What analysis can be done in this data?").
4. **Retrieve & Answer:** The assistant retrieves the top 10 most relevant rows (chunks) and prompts a large language model (LLM) to answer using *only* those data chunks.
5. **Get Results:** View the answer and the exact pandas code to reproduce it.

> **Note:** All answers are based on the top 10 most relevant chunks/rows from your CSV file for each question, ensuring data-grounded and efficient responses.

---

## 🧰 Tech Stack

- [Gradio](https://gradio.app/) for the interactive web UI
- [Pandas](https://pandas.pydata.org/) for data handling
- [LangChain](https://python.langchain.com/) for document loading and embeddings
- [Chroma](https://www.trychroma.com/) as the vector store for fast retrieval
- [HuggingFace Embeddings](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2) for semantic search
- [Groq LLM API](https://groq.com/) for answer generation


---

## 📑 Example Use Cases

- "What patterns cane be extracted from this column?"
- "List the top 5 customers by purchase amount."
- "Show the average, min, and max age of first 6 participants in the survey."

Each answer will be accompanied by pandas code you can copy into your notebook or script.

---

**CsvPal-AI**: https://huggingface.co/spaces/Tulika2000/CsvPal-AI
