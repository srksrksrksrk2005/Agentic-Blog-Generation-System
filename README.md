# Agentic AI Blog Writer

An end-to-end AI-powered blog generation system built with **LangGraph**, **LangChain**, and **Streamlit**. The application autonomously plans blog structure, performs web research, generates publication-ready blog posts, and manages supporting images through a multi-stage agent workflow.

> **Note**
> This project demonstrates modern LLM application development using agentic workflows, structured planning, retrieval pipelines, and interactive content generation.

---

# Features

## AI Planning

- Automatic blog outline generation
- Section-wise task planning
- Audience-aware content generation
- Tone customization
- Structured markdown generation

## Research Pipeline

- Automatic web research
- Evidence collection
- Source aggregation
- Citation-aware content generation

## Content Generation

- Long-form blog generation
- Markdown formatting
- Code block support
- Table generation
- Section-by-section writing

## Image Workflow

- Automatic image planning
- Local image management
- Markdown image embedding
- Downloadable image bundles

## Blog Management

- Persistent blog history
- Reload previously generated blogs
- Markdown export
- ZIP bundle export (Markdown + Images)

## User Interface

- Interactive Streamlit dashboard
- Live workflow progress
- Markdown preview
- Event logs
- Multi-tab interface

---

# Architecture

```text
                     User
                       │
                       ▼
                Streamlit Frontend
                       │
                       ▼
                LangGraph Workflow
                       │
 ┌──────────────┬──────────────┬──────────────┐
 ▼              ▼              ▼              ▼
Planning     Research     Blog Writer    Image Planner
                    │
                    ▼
            Web Search / Evidence
                    │
                    ▼
              Markdown Generator
                    │
                    ▼
            Export & Blog History
```

---

# Workflow

```text
Topic
 │
 ▼
Planning Agent
 │
 ▼
Research Decision
 │
 ├───────────────┐
 │               │
 ▼               ▼
Closed Book   Web Research
 │               │
 └──────┬────────┘
        ▼
Section Planning
        ▼
Section Generation
        ▼
Image Planning
        ▼
Markdown Assembly
        ▼
Preview & Export
```

---

# Project Structure

```text
blog-writer/
│
├── backend.py              # LangGraph workflow
├── frontend.py             # Streamlit application
├── images/                 # Generated images
├── requirements.txt
├── README.md
└── generated_blogs/
```

---

# Technologies

### AI Framework

- LangGraph
- LangChain

### Language Models

- OpenAI GPT Models

### Frontend

- Streamlit

### Data Processing

- Pandas

### Storage

- Markdown
- ZIP Archives

---

# Installation

Clone the repository:

```bash
git clone <repository-url>
cd blog-writer
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Create a `.env` file:

```env
OPENAI_API_KEY=YOUR_OPENAI_API_KEY
```

---

# Running the Application

Start the Streamlit application:

```bash
streamlit run frontend.py
```

The application will be available at:

```
http://localhost:8501
```

---

# Usage

1. Enter a blog topic.
2. Select the reference date.
3. Click **Generate Blog**.
4. The agent will:
   - Generate a writing plan
   - Decide whether web research is required
   - Collect supporting evidence
   - Generate each blog section
   - Create image specifications
   - Assemble the final markdown
5. Preview and download the generated blog.

---

# Interface

The application provides five interactive tabs:

| Tab | Description |
|------|-------------|
| 🧩 Plan | Blog outline and writing tasks |
| 🔎 Evidence | Research sources and collected evidence |
| 📝 Markdown Preview | Rendered markdown blog |
| 🖼️ Images | Generated image previews |
| 🧾 Logs | Workflow execution logs |

---

# Output

The application generates:

- Markdown blog
- Supporting images
- Downloadable Markdown file
- ZIP bundle containing Markdown and images

---

# Key Capabilities

- Agentic workflow orchestration
- Automatic research pipeline
- Structured blog planning
- Long-form markdown generation
- Image planning and management
- Persistent blog history
- Exportable publication-ready content

---

# Future Improvements

Potential enhancements include:

- Multi-agent collaboration
- SEO optimization
- Automatic keyword extraction
- Citation generation
- Multi-language blog generation
- WordPress and Medium publishing
- PDF export
- Docker deployment
- Local LLM support (Ollama / Llama.cpp)

---

# License

This project is licensed under the MIT License.
