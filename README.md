# NVIDIA DLI Final Project: Identifying Customer Complaint Sources with LLMs

This repository contains the final project for the NVIDIA DLI course, **"Building LLMs with Prompt Engineering."** This project demonstrates the use of Large Language Models (LLMs) and LangChain to perform automated analysis of customer feedback.

## 🎯 Project Objective

The goal of this project is to analyze a dataset of 10 fictitious customer emails from a retail store called "BuyBuy." The task is to build an automated pipeline that can:

1.  Read through all the customer emails.
2.  Determine the sentiment (positive or negative) of each email.
3.  Identify the **product category** and **store location** most frequently associated with negative customer feedback.
4.  Produce a concise, human-readable summary of the findings.

---

## 🛠️ Technologies & Concepts Used

This project leverages a multi-step, chained approach to process and analyze the data, showcasing several key concepts in prompt engineering and LLM application development:

* **Model**: `meta/llama-3.1-8b-instruct` served via NVIDIA AI Endpoints.
* **Core Framework**: **LangChain** for building the LLM pipeline.
* **Prompt Engineering**: Crafting specific prompts to instruct the LLM for different sub-tasks (analysis, formatting).
* **Structured Output**: Using `Pydantic` models and LangChain's `JsonOutputParser` to force the LLM to return structured, reliable data.
* **Chaining (LCEL)**: Combining multiple components (prompts, LLMs, parsers, Python functions) into a single, executable chain using the LangChain Expression Language (LCEL).
* **Data Processing**: A custom Python function (`RunnableLambda`) is integrated into the chain to aggregate and analyze the structured data from the LLM.

---
