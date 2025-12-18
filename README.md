# Multi-Agent Exploratory Data Analysis System

A **production-style, multi-agent exploratory data analysis (EDA) framework** built using **AutoGen**.  
This system coordinates multiple specialized AI agents to automatically **ingest data, perform structured EDA, generate visualizations, and produce a written analytical report**.

The project demonstrates practical skills in **agentic AI system design, LLM orchestration, and applied data analysis**, with a strong focus on **clarity, reproducibility, and real-world workflows**.

---

## Project Overview

Traditional EDA workflows require manual coordination between data cleaning, analysis, visualization, and reporting. This project reframes EDA as a **collaborative, role-based process**—similar to how data teams operate in practice.

Each agent is responsible for a distinct analytical role, and all agents interact through a managed group-chat architecture.

**Key goals of the system:**
- Modular, role-based agent design
- Clear separation of responsibilities
- Automated EDA with human-readable reporting
- Colab-friendly execution for rapid experimentation

---

## System Architecture

The system is implemented using an **AutoGen GroupChat** and includes the following agents:

### Agents

- **Admin**  
  Initiates tasks, provides high-level objectives, and approves the workflow.

- **DataProcesser**  
  Loads the dataset, performs basic validation and cleaning, and prepares data for analysis.

- **DataAnalyst**  
  Conducts exploratory analysis, generates statistical summaries, and produces visualizations.

- **ReportWriter**  
  Synthesizes analytical results into a structured EDA report with clear findings and interpretations.

- **Critic**  
  Reviews outputs for logical gaps, analytical quality, and clarity; provides feedback for refinement.

- **Executor**  
  Executes Python code produced by other agents (configured for Google Colab; Docker disabled).

This architecture mirrors real-world collaboration between data engineers, analysts, reviewers, and stakeholders.

---

## Key Features

- Multi-agent orchestration using AutoGen  
- Structured EDA workflow from raw data to final report  
- Automated visualization generation  
- Human-readable analytical summaries  
- Modular design that supports easy extension (modeling, validation, export formats)

---

## Quick Start (Google Colab)

1. Open `Multi_Agent_EDA_System.ipynb` in **Google Colab**
2. Install dependencies:
   ```bash
   !pip install -q autogen-agentchat==0.2.38
