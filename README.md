<<<<<<< HEAD
🧠 AI Research Paper Analyzer

An AI-powered web application that retrieves research papers from multiple academic sources and generates concise summaries using Large Language Models (LLMs), with MongoDB-based caching for improved performance and reduced API usage.

🚀 Features
🔍 Multi-source Paper Retrieval
Fetches research papers from:
arXiv
Semantic Scholar
🧾 AI-Based Summarization
Uses OpenAI API to generate concise summaries from abstracts
Designed to provide quick insights into research papers
🗄️ MongoDB Summary Caching
Stores generated summaries
Avoids recomputation for previously processed papers
Improves response time and reduces API cost
⚡ Efficient API Workflow
Checks database before calling OpenAI
Returns cached summaries instantly when available
🌐 Flask-Based Web Interface
Simple UI for searching and analyzing research papers

🏗️ System Architecture
User Query
   ↓
Flask API (app.py)
   ↓
Paper Fetcher (arXiv + Semantic Scholar)
   ↓
Check MongoDB (summary exists?)
   ↓            ↓
Yes ✅         No ❌
 ↓              ↓
Return       Generate Summary (OpenAI)
                 ↓
           Store in MongoDB
                 ↓
            Return Response

🧑‍💻 Tech Stack
Backend: Flask
Database: MongoDB Atlas
AI: OpenAI API
APIs: arXiv, Semantic Scholar
=======
# ResearchLens
An AI-powered research paper discovery and analysis platform that aggregates academic papers from multiple sources, generates concise AI-driven summaries, and uses intelligent caching to improve performance and reduce API costs.

## Overview

ResearchLens is designed to simplify the process of exploring academic literature. Instead of manually navigating multiple research platforms and reading lengthy abstracts, users can search for papers, retrieve relevant metadata, and obtain concise summaries generated using Large Language Models (LLMs).

The platform integrates academic paper repositories with AI-powered summarization and MongoDB-based caching to provide a faster and more efficient research workflow.

---

## Features

### Multi-Source Research Paper Retrieval

Search and retrieve papers from:

* arXiv
* Semantic Scholar

### AI-Powered Summarization

* Generates concise summaries from research paper abstracts
* Uses OpenAI models for natural language understanding and synthesis
* Provides quick insights without requiring users to read entire abstracts

### MongoDB Caching Layer

* Stores generated summaries in MongoDB
* Avoids repeated LLM calls for previously analyzed papers
* Reduces API costs and improves response times

### Modern Web Interface

* Responsive Flask-based web application
* Clean and intuitive user experience
* Built with HTML, CSS, and JavaScript

---

## System Architecture

```text
User Query
    │
    ▼
Flask Application
    │
    ▼
Paper Retrieval Layer
(arXiv + Semantic Scholar)
    │
    ▼
MongoDB Cache Check
    │
 ┌──┴───────────────┐
 │                  │
 ▼                  ▼
Cache Hit       Cache Miss
 │                  │
 ▼                  ▼
Return       OpenAI Summary Generation
                    │
                    ▼
             Store in MongoDB
                    │
                    ▼
              Return Result
```

---

## Tech Stack

### Backend

* Python
* Flask

### Database

* MongoDB Atlas
* PyMongo

### Artificial Intelligence

* OpenAI API

### External APIs

* arXiv API
* Semantic Scholar API

### Frontend

* HTML5
* CSS3
* JavaScript

---

## Project Structure

```text
ResearchLens/
│
├── app.py
├── requirements.txt
├── .env
│
├── src/
│   ├── db.py
│   ├── services/
│   │   ├── paper_fetcher.py
│   │   ├── paper_service.py
│   │   └── summarizer.py
│
├── templates/
│   └── index.html
│
├── static/
│   ├── style.css
│   └── script.js
│
└── tests/
```

---

## Installation

### Clone Repository

### Create Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

#### Windows

```bash
venv\Scripts\activate
```

#### macOS/Linux

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Environment Variables

Create a `.env` file in the project root.

```env
OPENAI_API_KEY=your_openai_api_key
MONGO_URI=your_mongodb_connection_string
```

---

## Run the Application

```bash
python app.py
```

The application will be available at:

```text
http://127.0.0.1:5000
```

---

## Future Enhancements

* PDF Upload and Analysis
* Keyword Extraction using NLP
* Semantic Similarity Search
* Research Topic Classification
* Vector Database Integration
* Citation Network Visualization
* Personalized Research Recommendations

---

## Motivation

Academic research is growing at an unprecedented rate, making it increasingly difficult to keep up with new publications. ResearchLens aims to bridge this gap by combining academic search with AI-powered summarization, enabling researchers and students to identify relevant work and understand it more efficiently.
>>>>>>> fe8242afc727b04528e5986d9e935e98868d0dfa
