## Overview
This notebook demonstrates implementing a research paper engine using the arXiv API to show how to improve LLM's response by augmenting LLM's knowledge with external data sources such as documents. The notebooks uses Vertex AI Gemini Pro 1.0 for Text, Embeddings for Text API, arXiv API and LangChain 🦜️🔗.

## Retrievel Augmented Genrative Model
Large Language Models (LLMs) have improved quantitatively and qualitatively. They can learn new abilities without being directly trained on them. However, there are constraints with LLMs - they are unaware of events after training and it is almost impossible to trace the sources to their responses. It is preferred for LLM based systems to cite their sources and be grounded in facts.

To solve for the constraints, one of the approaches is to augment the prompt sent to LLM with relevant data retrieved from an external knowledge base through Information Retrieval (IR) mechanism.

This approach is called Retrieval Augmented Generation (RAG), also known as Generative QA in the context of a Question Answering task. There are two main components in RAG based architecture: (1) Retriever and (2) Generator.
