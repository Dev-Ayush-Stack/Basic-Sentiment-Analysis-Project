# 🧠 Sentiment Analysis & Text Classification App

## 📌 Overview

This project is a **Language Model (LLM)-powered text classification system** built using **LangChain** and **Groq API**(Using open-source model from open-ai via grok->Note:-Always watch out for depricated models and their replacements).

It analyzes a given text passage and extracts structured information including:

* Sentiment
* Political Tendency
* Language

The output is generated in a **structured format using Pydantic schema**, ensuring consistency and reliability.

---

## 🚀 Features

* 🔍 **Sentiment Analysis** (positive/negative/neutral-like understanding)
* 🏛️ **Political Tendency Detection**
* 🌍 **Language Identification**
* 🧩 **Structured Output using Pydantic**
* ⚡ **Fast inference using Groq LLM**
* 🔗 **LangChain pipeline (Prompt → Model → Output)**

---

## 🛠️ Tech Stack

* **Python**
* **LangChain**
* **Groq API (LLM)**
* **Pydantic**
* **Jupyter Notebook**
* **Poetry (Dependency Management)**

---

## 📂 Project Structure

```
Sentiment-Analysis-Project/
│── basic-schema.ipynb        # Main notebook (core logic)
│── pyproject.toml            # Poetry dependencies
│── poetry.lock
│── .env                      # API keys (ignored)
│── .gitignore
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/sentiment-analysis-app.git
cd sentiment-analysis-app
```

---

### 2️⃣ Install Dependencies (Poetry)

```bash
poetry install
```

---

### 3️⃣ Activate Environment

```bash
poetry shell
```

---

### 4️⃣ Setup Environment Variables

Create a `.env` file:

```env
Free_API_KEY=your_groq_api_key_here
```

---

## ▶️ Usage

Run the notebook or use the chain directly:

```python
response = tagging_chain.invoke({
    "input": "I absolutely love this new phone. The battery life is amazing!"
})

print(response)
```

---

## 📊 Example Outputs

### ✅ Positive Input

```python
Input:
"I absolutely love this new phone."

Output:
sentiment='positive'
political_tendency='neutral'
language='English'
```

---

### ❌ Negative Input

```python
Input:
"This service is terrible."

Output:
sentiment='negative'
political_tendency='neutral'
language='English'
```

---

### 🏛️ Political Input

```python
Input:
"The government should invest more in education."

Output:
sentiment='neutral'
political_tendency='liberal'
language='English'
```

---

## 🧠 How It Works

1. **Prompt Template** defines extraction rules
2. **Pydantic Schema** enforces structured output
3. **LangChain Chain** connects:

   ```
   Prompt → LLM → Structured Output
   ```
4. **Groq LLM** processes input and returns classification

---

## 🔒 Security Note

* `.env` file is ignored using `.gitignore`
* API keys are kept secure and not exposed in the repository

---

## 🚀 Future Improvements

* Add **Streamlit UI**
* Expand language support
* Improve classification accuracy with fine-tuning
* Add REST API (FastAPI)

---

## 👨‍💻 Author

**Ayush Pandey**

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and share it!
