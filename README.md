# 🧠 GenAI Summarizer App — YouTube, Web, and Docs  
**LangChain + Groq + Streamlit**

> ⚠️ **Note:** YouTube links may not work on Streamlit Cloud due to IP restrictions imposed by YouTube.  
> To summarize YouTube videos, **run this app locally**.

---

## ✨ What It Does

A powerful Generative AI app to summarize:
- 📺 **YouTube videos** (via transcript)
- 🌐 **Web pages** (via URL)
- 📄 **Documents** using LangChain’s summarization chains

Supports:
- `stuff`
- `map_reduce`
- `refine`

---

## ⚙️ Tech Stack

- 🧠 **LangChain** — prompt orchestration + document loaders  
- ⚡ **Groq LLM (Gamma)** — blazing-fast summarization  
- 🎛 **Streamlit** — sleek, interactive frontend UI  

---

## 🚀 Features

✅ Summarize YouTube videos and website articles  
✅ Choose between `stuff`, `map_reduce`, or `refine`  
✅ Multi-language summaries (e.g., Hindi, French)  
✅ Secure API key input via sidebar  
✅ Real-time input validation & helpful error handling  
✅ Optional LangSmith tracing (tokens, latency, cost)

---

## 🧪 Summarization Strategies

| Chain Type    | Behavior                                       | Best For                            |
|---------------|------------------------------------------------|-------------------------------------|
| `stuff`       | Summarize everything in one go                 | Small or short documents            |
| `map_reduce`  | Summarize chunks first, then combine results   | Medium to large content             |
| `refine`      | Build a summary incrementally, chunk by chunk  | Long, structured documents          |

---

## 📈 (Optional) LangSmith Tracing

Track and debug LLM usage:

1. Create an account: https://smith.langchain.com  
2. Add this to your `.env`:

```env
LANGCHAIN_TRACING_V2=true  
LANGCHAIN_API_KEY=your_langsmith_key  
LANGCHAIN_PROJECT=genai-summarizer


3. Add callback like:
   
from langchain.callbacks.tracers import LangChainTracer
tracer = LangChainTracer(project_name="genai-summarizer")
response = chain.run(..., callbacks=[tracer])




