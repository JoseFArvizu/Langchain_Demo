
# 🧠 Simple LangChain Demo

This project demonstrates a basic usage of [LangChain](https://www.langchain.com/) to interact with large language models through a custom Python notebook. It is intended for educational or experimental use with OpenAI's API.

## 📁 Files

- `Simple_Langchain.ipynb`: Main Jupyter notebook that demonstrates how to use LangChain to run a simple chatbot-style prompt with memory.
- `config.py`: Stores your OpenAI API key securely.

## 🚀 Features

- Integrates LangChain's `ConversationChain` for interactive AI responses.
- Uses OpenAI's GPT model via the `OpenAI` LangChain wrapper.
- Tracks conversation history with `ConversationBufferMemory`.
- API key is externalized for better security and flexibility.

## 🛠️ Installation

Before running the notebook, make sure you have the following Python libraries installed:

```bash
pip install langchain openai
```

We also recommend installing Jupyter if you're not using an IDE that supports notebooks:

```bash
pip install notebook
```

## 🔐 API Key Setup

Update the `config.py` file with your actual OpenAI API key:

```python
api_key = 'your_openai_api_key_here'
```

**⚠️ Never share your actual API key publicly.**

## ▶️ Usage

1. Clone the repository or download the files.
2. Open `Simple_Langchain.ipynb` using Jupyter Notebook or any compatible IDE.
3. Run the notebook step by step. It will:
   - Load your API key
   - Initialize the OpenAI LLM and LangChain memory
   - Allow you to chat with the LLM using conversational context

## 📌 Example Code Snippet

```python
from langchain.llms import OpenAI
from langchain.chains import ConversationChain
from langchain.memory import ConversationBufferMemory
from config import api_key

llm = OpenAI(openai_api_key=api_key)
memory = ConversationBufferMemory()
conversation = ConversationChain(llm=llm, memory=memory)

response = conversation.predict(input="Hello, who won the world cup?")
print(response)
```

## 📎 License

This project is provided for educational use. Refer to OpenAI and LangChain license terms for production use.
