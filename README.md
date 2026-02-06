# AI_Projects
A collection of AI projects exploring RAG, LLMs, OCR, and citation-aware systems for real-world applications.


🛡️ Agentic RAG-Based Email Threat Detection System
📌 Overview

This project implements an Agentic Retrieval-Augmented Generation (RAG) powered email classification system designed to detect phishing, fraud, brand impersonation, and business email compromise (BEC) attacks in real-world email content.Unlike traditional keyword-only spam filters, this system combines rule-based reasoning, machine learning, semantic similarity (RAG), and brand/domain reputation analysis to accurately classify emails as SAFE, SUSPICIOUS, or MALICIOUS.
The architecture mirrors how modern enterprise email security platforms (e.g., Microsoft Defender, Proofpoint, Mimecast) operate.

🚀 Key Features
🔍 Multi-Agent Detection Pipeline
    The system uses independent analytical agents, each specializing in a different threat dimension:
        Rule-Based Agent
            Detects urgency pressure, credential theft patterns, financial fraud, and BEC indicators
            Uses structured threat keyword taxonomies (phishing, billing fraud, advance-fee scams, etc.)
        Domain & Brand Impersonation Agent
            Detects brand misuse even without sender email
            Flags mismatched sender domains for brands like Apple, Amazon, Microsoft, Google, banks, ISPs, and government bodies
            Supports hard overrides for high-confidence impersonation
        Machine Learning Agent
            Lightweight TF-IDF + RandomForest classifier
            Adds probabilistic risk scoring for phishing-like language patterns
        RAG Semantic Similarity Agent
            Uses SentenceTransformers to match email content against known phishing attack narratives
            Detects semantic intent beyond exact keywords

🧠 Agentic Risk Scoring
      Each agent produces a risk score that is combined using weighted orchestration logic:
            Rule-based signals (highest weight)
            ML classification
            Semantic similarity (RAG)
            Brand/domain reputation
      Final classification:
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
    This system detects:
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
      Suitable for cybersecurity labs, internships, SOC training, and academic projects
  Note: Accuracy depends on dataset quality and threshold tuning.

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
    Academic projects (cyber security)
    Email threat research
    AI-based security experimentation
