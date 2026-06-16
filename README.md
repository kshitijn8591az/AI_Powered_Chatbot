# 🤖 AI~Buddy

AI~Buddy is an AI-powered chatbot built using **LangChain**, **Groq LLM**, **Google Search**, and **Streamlit**. It provides conversational AI capabilities with real-time web search and streaming responses through a simple web interface.

---

## 🚀 Features

* 💬 Interactive chatbot UI using Streamlit
* 🤖 Powered by Groq LLM (`openai/gpt-oss-20b`)
* 🔍 Real-time Google Search integration
* ⚡ Streaming responses for improved user experience
* 🧠 Conversation memory using LangGraph MemorySaver
* 🔄 Context-aware conversations
* 🌐 Ability to retrieve up-to-date information from the web

---

## 🏗️ Architecture

```text
User
  │
  ▼
Streamlit UI
  │
  ▼
LangChain Agent
  │
  ├──► Groq LLM
  │
  └──► Google Search (Serper API)
  │
  ▼
Streaming Response
  │
  ▼
MemorySaver (Conversation History)
```

---

## 🛠️ Tech Stack

| Component       | Technology            |
| --------------- | --------------------- |
| Frontend        | Streamlit             |
| LLM             | Groq (GPT-OSS-20B)    |
| Agent Framework | LangChain             |
| Memory          | LangGraph MemorySaver |
| Search Engine   | Google Serper API     |
| Language        | Python                |

---

## 📂 Project Structure

```text
project/
│
├── qna_bot.py
├── .env
├── requirements.txt
└── README.md
```

---

## ⚙️ Prerequisites

Before running the application, obtain the following API keys:

### Groq API Key

https://console.groq.com

### Google Serper API Key

https://serper.dev

---

## 🔐 Environment Variables

Create a `.env` file in the project root.

```env
GROQ_API_KEY=your_groq_api_key
SERPER_API_KEY=your_serper_api_key
```

---

## 📦 Installation

### Clone Repository

```bash
git clone https://github.com/your-username/ai-buddy.git

cd ai-buddy
```

### Create Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

**Windows**

```bash
venv\Scripts\activate
```

**Linux/Mac**

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 📋 Required Packages

```bash
pip install streamlit
pip install langchain
pip install langgraph
pip install langchain-groq
pip install langchain-community
pip install google-search-results
pip install python-dotenv
```

---

## ▶️ Running the Application

```bash
streamlit run qna_bot.py
```

Application will be available at:

```text
http://localhost:8501
```

---

## 🔄 How It Works

1. User enters a query through the Streamlit interface.
2. LangChain Agent receives the request.
3. Agent determines whether external information is required.
4. If needed, Google Search is invoked through Serper API.
5. Groq LLM generates a response.
6. Response is streamed token-by-token to the UI.
7. Conversation history is stored using MemorySaver.

---

## 💡 Example Questions

* What is the capital of Japan?
* Latest AI news today
* Explain Retrieval Augmented Generation (RAG)
* Who won the latest IPL match?
* Compare Spark and Polars

---

## 🔮 Future Enhancements

* 📄 RAG with PDF and document search
* 🤝 Multi-agent workflows
* 🎙️ Voice-based interactions
* 📊 Analytics dashboard
* 🔐 User authentication
* 📚 Wikipedia and database integrations
* 🛡️ AI safety guardrails
* 🧠 Long-term memory support

---

## 📸 Demo

```text
AI~Buddy
---------------------------------
User: Latest AI news today?

AI: Searching Google...
    Here are the latest updates...
```

---

## 👨‍💻 Author

Developed as an AI-powered conversational assistant using LangChain, Groq, and Streamlit.
