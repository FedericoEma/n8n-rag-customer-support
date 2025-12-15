# n8n-rag-customer-support
AI Support Agent using RAG (Supabase) to answer rulebook questions with Zendesk fallback integration.

Disclaimer: This project is a personal tech demo for educational purposes only. It is not affiliated with, endorsed by, or connected to Editrice Giochi, Spin Master, or the official RisiKo! brand. All trademarks and copyrights belong to their respective owners.

# AI Rule Assistant (Demo on Risiko Rules) 🤖

<img width="1661" height="540" alt="Screenshot (75)" src="https://github.com/user-attachments/assets/02046f1e-f3e6-4ffa-b0bd-2ff916b923a4" />

## 📋 Overview
This project is an advanced AI automation workflow built in **n8n**. It acts as a specialized customer support agent capable of answering complex questions based on a specific PDF manual (RAG), with a robust fallback mechanism to human operators.

## 🚀 Key Features
* **RAG Architecture:** Uses **Supabase** (Vector Store) to retrieve accurate answers from the official rulebook.
* **Human-in-the-loop:** If the confidence is low or the info is missing, it automatically creates a ticket in **Zendesk**.
* **Analytics:** Logs every interaction in **Airtable** for performance monitoring.
* **Reporting:** Generates and emails weekly PDF reports via **Google Docs/Gmail**.

## 🛠️ Tech Stack
* **Orchestration:** n8n
* **LLM:** Google Gemini / OpenAI
* **Vector Database:** Supabase
* **Tools:** Zendesk, Airtable, Google Workspace

## ⚙️ How it Works
1.  **Ingestion:** The user asks a question via Chat Interface.
2.  **Retrieval:** The system searches vector embeddings in Supabase.
3.  **Generation:** The LLM formulates an answer based *only* on retrieved context.
4.  **Fallback:** If no answer is found, a Zendesk ticket is raised.
5.  **Logging:** Data is stored for analysis.

## 📦 How to use
Import the `workflow.json` file directly into your n8n instance.
