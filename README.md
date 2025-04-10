# 💜 HerVoice – AI Chatbot Empowering Women in STEM

HerVoice is an AI-powered support assistant designed to empower women in STEM (Science, Technology, Engineering, and Mathematics). It provides a safe and anonymous space for mentorship, career guidance, emotional support, and navigating workplace challenges.

---
## ✨ Features

- 🤖 **Conversational Agent** built with Google Gemini for empathetic and informative support  
- 🔍 **Multi-query Retrieval-Augmented Generation (RAG)** with MMR and RRF for accurate answers  
- 📚 **Custom Vector Database** using `PGVector` to index curated resources and books  
- 🌐 **Tavily Web Search** integration for current, real-world information  
- ✅ **Answer Verification** using hallucination and relevance grading  
- 🧠 **Query Rewriting** for improving search coverage  
- 🎨 **Streamlit Frontend** with a feminine and empowering aesthetic  

---

## 🛠️ Tech Stack

| Component    | Technology                              |
|--------------|------------------------------------------|
| LLM          | Google Gemini (via `langchain_google_genai`) |
| Vector Store | PostgreSQL + pgvector                    |
| Embeddings   | GoogleGenerativeAIEmbeddings             |
| Frontend     | Streamlit                                |
| Web Search   | Tavily API                               |
| Orchestration| LangGraph                                |

---

## Poetry Setup

Create a local virtual environment with Poetry using
```
 poetry config virtualenvs.in-project true
```
Then, `cd` into the directory that contains pyproject.toml and poetry.lock. Install the poetry environment with this terminal command:
```
poetry install
```

## Gemini Setup
You need an `.env` file with these values set up:
```
export GEMINI_API_KEY="something"
export DB_CONNECTION= "postgresql+psycopg://something"
export GOOGLE_APPLICATION_CREDENTIALS="something.json"
export DEFAULT_GOOGLE_PROJECT="something"
export GOOGLE_CLOUD_LOCATION=us-central1
export GOOGLE_GENAI_USE_VERTEXAI=True

```

You also need the JSON file that is mentioned in `GOOGLE_APPLICATION_CREDENTIALS`.

# To preprocess and embed PDFs into the vectorstore:

```python Knowledge.py```

# Launch the Chatbot

```streamlit run HerVoice.py```