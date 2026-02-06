# AI_Projects
A collection of AI projects exploring RAG, LLMs, OCR, and citation-aware systems for real-world applications.


🛡️ Agentic RAG-Based Email Threat Detection System
📌 Overview
This project implements an Agentic Retrieval-Augmented Generation (RAG) powered email threat detection system designed to identify:

Phishing attacks

Fraudulent communications

Brand impersonation

Business Email Compromise (BEC)

Unlike traditional keyword-only spam filters, the system combines:

Rule-based reasoning

Machine learning classification

Semantic similarity using RAG

Brand and domain reputation analysis

Emails are classified into:

SAFE

SUSPICIOUS

MALICIOUS

The architecture is inspired by modern enterprise email security platforms such as Microsoft Defender, Proofpoint, and Mimecast.

🚀 Key Features
🔍 Multi-Agent Detection Pipeline

The system uses independent analytical agents, each responsible for a different threat dimension:

🧩 Rule-Based Agent

Detects urgency pressure, credential theft patterns, financial fraud, and BEC indicators

Uses structured threat keyword taxonomies:

Phishing

Billing fraud

Advance-fee scams

Security impersonation

🌐 Domain & Brand Impersonation Agent

Detects brand misuse even when sender email is missing

Flags mismatched sender domains for major brands:

Apple, Amazon, Microsoft, Google

Banks, ISPs, government entities

Supports hard overrides for high-confidence impersonation attacks

🤖 Machine Learning Agent

Lightweight TF-IDF + RandomForest classifier

Adds probabilistic risk scoring based on phishing-like language patterns

📚 RAG Semantic Similarity Agent

Uses SentenceTransformers to compare emails against known phishing narratives

Detects semantic intent beyond exact keyword matches

🧠 Agentic Risk Scoring

Each agent produces a risk score that is combined using weighted orchestration logic:

Rule-based signals (highest weight)

Machine learning classification

Semantic similarity (RAG)

Brand and domain reputation

Final Classification

SAFE

SUSPICIOUS

MALICIOUS

Hard overrides ensure that critical impersonation attacks are never misclassified as safe.

🛠️ Technologies Used

Python

LangChain (Agentic RAG concepts)

SentenceTransformers

scikit-learn

RandomForestClassifier

TF-IDF Vectorization

Regex-based preprocessing

FAISS / Vector embeddings (optional extension)

🧪 Threat Coverage

The system detects:

✔ Phishing & credential harvesting

✔ Brand impersonation (Apple, Amazon, Microsoft, Google, banks, ISPs)

✔ Billing & payment fraud

✔ Advance-fee / inheritance scams

✔ Business Email Compromise (BEC)

✔ Meeting link & calendar abuse

✔ Fake security vendor notifications

✔ Urgency & pressure-based social engineering

📈 Accuracy & Performance

Designed to achieve ~80–88% detection accuracy on real-world phishing datasets

Optimized for high recall on malicious emails

Suitable for:

Cybersecurity labs

Internships

SOC training

Academic projects

Note: Accuracy depends on dataset quality, thresholds, and real-world variability.

💻 How It Works

User inputs raw email content

Preprocessing extracts:

URLs

Sender domains

Keywords

Urgency indicators

Each agent independently analyzes the email

Risk scores are aggregated

Final classification and evidence are returned in real time

🧑‍💻 Use Cases

SOC analyst training

Cybersecurity internships

Academic projects (Cyber Security / AI)

Email threat research

AI-based security experimentation
