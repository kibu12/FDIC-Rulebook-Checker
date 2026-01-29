---

# 🏦 AI Assistant for Bank Loan Review

**FDIC Rulebook Checker (Section 3.2)**

A regulatory-aligned AI system that analyzes loan documents using **only** the FDIC RMS Manual – Section 3.2.
It provides risk observations and compliance insights via a **Gradio web interface**, without making approval or rejection decisions.

---

## 📌 Features

* 📄 Upload loan documents (PDF or TXT)
* 🧠 AI analysis strictly based on **FDIC Section 3.2**
* 📑 Automatic **10-line factual loan summary**
* ❓ Ask regulatory questions about the loan
* 🚫 No hallucinations – out-of-scope queries are refused
* ⚖️ Advisory only (no approve/reject decisions)
* 🌐 Web UI built using **Gradio**

---

## 🧠 System Design

### Core Principles

| Rule            | Description                                 |
| --------------- | ------------------------------------------- |
| Source of Truth | Only FDIC RMS Manual – Section 3.2          |
| Role            | Regulatory Loan Review Assistant            |
| Output          | Risks, gaps, examiner observations          |
| Prohibited      | Approval, rejection, legal/financial advice |
| Interface       | Web-based (Gradio)                          |

---

## 🛠 Tech Stack

* **Python 3**
* **OpenAI API**
* **Gradio** – Web UI
* **PyPDF** – PDF text extraction
* **Google Colab** (optional)

---

## 📂 Project Structure

```
.
├── app.ipynb / app.py
├── FDIC_SECTION.txt
├── README.md
└── requirements.txt
```

---

## ⚙️ Installation

### 1️⃣ Install dependencies

```bash
pip install gradio pypdf openai
```

Or create `requirements.txt`:

```txt
gradio
pypdf
openai
```

---

### 2️⃣ Add FDIC rulebook

Save the FDIC manual text as:

```
FDIC_SECTION.txt
```

---

### 3️⃣ Configure API Key

For Colab:

```python
from google.colab import userdata
```

Add:

```
API_KEY
BASE_URL (optional)
```

Or set environment variable:

```bash
export OPENAI_API_KEY="your_key_here"
```

---

## ▶️ Running the App

If using Python:

```bash
python app.py
```

If using Jupyter/Colab:

Run all cells → Gradio will generate a public URL.

---

## 🖥 How to Use

1. Upload a loan document (PDF or TXT)
2. Click **Summarize Document**
3. Ask a regulatory question
4. Receive FDIC-aligned analysis

---

## 🔐 Safety & Compliance

This system:

* Does NOT approve or reject loans
* Does NOT provide legal or financial advice
* Does NOT use external knowledge beyond FDIC Section 3.2
* Refuses out-of-scope questions

---

## 📊 Example Output

* Property description completeness
* Missing appraisal details
* Documentation gaps
* Collateral adequacy
* Underwriting deviations

All based strictly on FDIC guidance.

---

## 🚀 Future Improvements

* Vector search for faster rule lookup
* Multi-section FDIC support
* Audit trail logging
* User authentication
* Deployment to HuggingFace Spaces / Streamlit Cloud

---

## ⚠️ Disclaimer

This tool is for **educational and research purposes only**.
It does not replace professional regulatory judgment or official compliance reviews.

---
