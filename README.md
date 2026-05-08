# AI Job Search Agent

AI-powered job search and resume optimization system that uses LLM-driven reasoning, tool orchestration, and workflow automation to filter opportunities, rank job matches, and tailor resumes for specific roles.

This project demonstrates how AI agents can automate parts of the modern job application workflow using structured reasoning, retrieval pipelines, and resume adaptation techniques.

---

# Tech Stack

`Python` `LLMs` `Gemini API` `Groq API` `NLP` `AI Agents` `Automation` `Pandas`

---

# Project Overview

The system implements a single-agent workflow that:

- loads candidate profiles and job datasets
- filters relevant opportunities
- ranks jobs based on candidate fit
- selects the strongest match
- generates tailored resume content for the selected role

The workflow combines:
- LLM reasoning
- tool calling
- structured ranking logic
- automated resume tailoring

---

# Features

- AI-driven job filtering
- Job ranking and scoring workflows
- Resume tailoring automation
- Tool-based agent orchestration
- Structured reasoning traces
- Artifact generation for downstream review

---

# Repository Structure

```text
ai-job-search-agent/
├── main.py
├── requirements.txt
├── README.md
├── data/
├── tools/
├── scripts/
├── tests/
└── artifacts/
```

---

# Core Components

## Agent Orchestration

`main.py`
- coordinates the full agent workflow
- manages tool execution
- handles reasoning flow and output generation

---

## Filtering Tool

`tools/filtering.py`
- narrows the job list using candidate preferences and constraints

---

## Ranking Tool

`tools/ranking.py`
- scores filtered jobs
- ranks opportunities based on relevance and fit

---

## Resume Tailoring Tool

`tools/tailoring_resume.py`
- rewrites resume summaries
- adapts experience bullet points
- optimizes content for target job alignment

---

## Dataset Generation

`scripts/scrape_jobs.py`
- generates job datasets and supporting inputs
- supports optional dataset regeneration workflows

---

# Installation

## Create Virtual Environment

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

---

# Environment Variables

Set required API keys before running:

```bash
export GEMINI_API_KEY="your_gemini_api_key"
export GROQ_API_KEY="your_groq_api_key"
```

Optional dataset regeneration:

```bash
export SERPAPI_KEY="your_serpapi_key"
```

---

# Running The Project

Run the complete agent workflow:

```bash
python main.py
```

---

# Expected Workflow

The agent performs the following sequence:

1. Load candidate profile and job dataset
2. Filter relevant job opportunities
3. Rank jobs based on candidate fit
4. Select the best-matching role
5. Generate tailored resume content
6. Save reasoning traces and outputs

---

# Generated Outputs

The system writes structured outputs to:

```text
artifacts/
```

Generated artifacts include:

- reasoning traces
- ranked job outputs
- filtered job datasets
- tailored resume JSON
- tailored resume text outputs

---

# Input Data

Primary inputs:

- candidate profile
- base resume
- job posting dataset

Stored under:

```text
data/
```

---

# Testing

Run tests individually:

```bash
pytest tests/test_filtering.py -q
pytest tests/test_ranking.py -q
pytest tests/test_main.py -q
```

---

# Skills Demonstrated

- AI agent orchestration
- LLM workflow automation
- Tool-calling systems
- Resume optimization pipelines
- NLP workflows
- Structured ranking systems
- Python backend development
- Automation engineering

---

# Limitations

- Current workflow uses a single-agent architecture
- Resume tailoring quality depends on LLM outputs
- Ranking logic is heuristic-based rather than learned
- External API availability affects runtime reliability

---

# Future Improvements

- Multi-agent orchestration
- Real-time job ingestion pipelines
- Vector search for semantic matching
- User feedback learning loops
- Web application deployment
- Advanced ATS optimization workflows

---

# Notes

- API keys and sensitive environment variables were excluded from the repository.
- Large generated artifacts and datasets were minimized for GitHub upload.
- This project was originally developed as part of an AI systems engineering assignment and later cleaned into a portfolio-ready implementation.
