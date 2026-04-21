# Installation and Setup

This guide covers environment creation, dependency installation, and running the Streamlit app.

## 1. Prerequisites

- Python 3.10 or newer
- pip
- Internet access (for package downloads and API calls)

## 2. Create and activate a virtual environment

From the project root:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

## 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## 4. Configure environment variables

Create a `.env` file in the project root with your API key:

```env
GROQ_API_KEY='YOUR_API_KEY'
```

## 5. Run the Streamlit app

```bash
streamlit run streamlit_frontend.py
```

Then open the local URL shown in the terminal (usually http://localhost:8501).

## 6. Optional: deactivate environment

```bash
deactivate
```

## Notes

- Conversation state is stored in `chatbot.db` (SQLite).
- Upload PDFs from the sidebar after the app starts.
