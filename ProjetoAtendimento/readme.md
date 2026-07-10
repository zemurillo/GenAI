
# Projeto de Atendimento e Suporte com RAG

> 🇧🇷 **Versão em Português**  
> 🇺🇸 **English version below**

> **Nota:** Este projeto foi desenvolvido durante as aulas de um curso sobre **Inteligência Artificial Generativa e Agentes**, com finalidade educacional e de aprendizado prático. O objetivo é aplicar conceitos como LLMs, Retrieval-Augmented Generation (RAG), embeddings, bancos vetoriais e frameworks para desenvolvimento de aplicações baseadas em IA Generativa.

## Objetivo

Este projeto implementa um chatbot de atendimento e suporte utilizando **Retrieval-Augmented Generation (RAG)**, com foco em responder perguntas com base em documentos reais da empresa, como PDFs, manuais e bases de conhecimento.

O assistente é capaz de:

- Responder dúvidas de clientes e colaboradores;
- Buscar informações em documentos estruturados;
- Fornecer respostas mais precisas do que um modelo de linguagem sem contexto;
- Servir como base para uma interface simples desenvolvida com Streamlit.

## Contexto do projeto

O projeto foi desenvolvido a partir do notebook **"2 - LLMs para empresas e negócios - Atendimento e Suporte.ipynb"**, que demonstra:

- Uso de modelos de linguagem (LLMs);
- Carregamento e processamento de documentos PDF;
- Divisão de texto em chunks;
- Geração de embeddings;
- Indexação utilizando FAISS;
- Recuperação de contexto com LangChain;
- Geração de respostas fundamentadas nos documentos recuperados.

## Tecnologias utilizadas

- Python
- LangChain
- LangChain Community
- LangChain Groq / OpenAI
- FAISS
- Sentence Transformers
- PyMuPDF
- Streamlit
- Python Dotenv

## Fluxo da aplicação

1. Carregamento dos documentos PDF;
2. Extração do conteúdo textual;
3. Divisão do texto em pequenos blocos (chunks);
4. Geração dos embeddings;
5. Armazenamento no banco vetorial FAISS;
6. Recuperação dos trechos mais relevantes para cada pergunta;
7. Geração da resposta utilizando o contexto recuperado.

## Pré-requisitos

- Python 3.9 ou superior
- Chave de API da Groq ou OpenAI
- Ambiente virtual (recomendado)

## Instalação

```bash
pip install -q langchain-core==0.3.1
pip install -q langchain==0.3.1
pip install -q langchain-community==0.3.1
pip install -q langchain-huggingface==0.1.1
pip install -q faiss-cpu==1.10.0
pip install -q sentence-transformers==3.1.0
pip install -q langchain-classic
pip install -q langchain_groq PyMuPDF
pip install -q streamlit python-dotenv
pip install -q numpy==1.26.3
```

## Configuração

Configure as variáveis de ambiente com suas chaves de API:

```bash
export GROQ_API_KEY="sua-chave"
export OPENAI_API_KEY="sua-chave"
```

Ou utilize um arquivo `.env` na raiz do projeto.

## Como executar

Execute o notebook para testar toda a pipeline RAG.

Para iniciar a interface web com Streamlit:

```bash
streamlit run app02.py
```

## Estrutura do projeto

```
.
├── documentos/
├── app02.py
└── 2 - LLMs para empresas e negócios - Atendimento e Suporte.ipynb
```

## Observações

- Projeto desenvolvido para fins educacionais e demonstração de uma arquitetura RAG.
- Em ambientes de produção, recomenda-se adicionar autenticação, monitoramento, tratamento de erros e mecanismos para validação das respostas.
- A qualidade das respostas depende diretamente da qualidade dos documentos indexados.

---

# Customer Support Chatbot with RAG

> **Note:** This project was developed during a **Generative AI and AI Agents** course as a hands-on educational exercise. Its purpose is to apply concepts such as LLMs, Retrieval-Augmented Generation (RAG), embeddings, vector databases, and modern frameworks for building Generative AI applications.

## Objective

This project implements a customer support chatbot using **Retrieval-Augmented Generation (RAG)** to answer questions based on real company documents such as PDFs, manuals, and knowledge bases.

The assistant is designed to:

- Answer questions from customers and employees;
- Retrieve information from structured documents;
- Provide more accurate responses than a standalone language model;
- Serve as the backend for a simple Streamlit interface.

## Project Background

The project was built from the notebook **"2 - LLMs for Business - Customer Support.ipynb"**, demonstrating:

- Large Language Models (LLMs);
- PDF loading and processing;
- Text chunking;
- Embedding generation;
- FAISS vector indexing;
- Context retrieval using LangChain;
- Context-aware response generation.

## Technologies

- Python
- LangChain
- LangChain Community
- LangChain Groq / OpenAI
- FAISS
- Sentence Transformers
- PyMuPDF
- Streamlit
- Python Dotenv

## Application Workflow

1. Load PDF documents;
2. Extract document text;
3. Split the content into chunks;
4. Generate embeddings;
5. Store embeddings in a FAISS vector database;
6. Retrieve the most relevant chunks;
7. Generate a final answer using the retrieved context.

## Requirements

- Python 3.9+
- Groq or OpenAI API Key
- Virtual environment (recommended)

## Installation

```bash
pip install -q langchain-core==0.3.1
pip install -q langchain==0.3.1
pip install -q langchain-community==0.3.1
pip install -q langchain-huggingface==0.1.1
pip install -q faiss-cpu==1.10.0
pip install -q sentence-transformers==3.1.0
pip install -q langchain-classic
pip install -q langchain_groq PyMuPDF
pip install -q streamlit python-dotenv
pip install -q numpy==1.26.3
```

## Configuration

Set your API keys as environment variables:

```bash
export GROQ_API_KEY="your-key"
export OPENAI_API_KEY="your-key"
```

Alternatively, use a `.env` file.

## Running the Project

Run the notebook to test the complete RAG pipeline.

To start the Streamlit interface:

```bash
streamlit run app02.py
```

## Project Structure

```
.
├── documentos/
├── app02.py
└── 2 - LLMs para empresas e negócios - Atendimento e Suporte.ipynb
```

## Notes

- This is an educational implementation intended to demonstrate a RAG architecture.
- Production deployments should include authentication, monitoring, error handling, and response validation.
- Response quality depends heavily on the quality of the indexed documents.
