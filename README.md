# AI Candidate Discovery & Ranking System

An AI-powered candidate discovery and ranking system built for the **Redrob AI Intelligent Candidate Discovery & Ranking Challenge**.

Instead of relying on traditional keyword matching, this project uses **semantic search, dense embeddings, FAISS retrieval, and hybrid scoring** to identify candidates who truly fit a job description.

---

# Problem Statement

Traditional Applicant Tracking Systems (ATS) depend heavily on keyword matching, often missing qualified candidates who express their experience differently.

This project aims to rank candidates the way an experienced recruiter would by considering:

* Semantic similarity between candidate profile and job description
* Relevant technical skills
* Professional experience
* Recruiter engagement signals
* Candidate availability
* Behavioral indicators

---

# Solution Architecture

```
Job Description
       │
       ▼
Sentence Transformer Embedding
       │
       ▼
Semantic Vector Representation
       │
       ▼
FAISS Similarity Search
       │
       ▼
Top 2,000 Candidates
       │
       ▼
Hybrid Ranking Engine
 ┌──────────────┬───────────────┬──────────────┐
 │ Semantic     │ Behavioral    │ Experience   │
 │ Score        │ Signals       │ Matching     │
 └──────────────┴───────────────┴──────────────┘
       │
       ▼
Final Candidate Score
       │
       ▼
Top 100 Ranked Candidates
```

---

# Features

* Semantic candidate matching using Sentence Transformers
* Dense vector retrieval with FAISS
* Hybrid candidate ranking
* Recruiter-aware behavioral scoring
* Experience-aware ranking
* Availability and notice-period scoring
* Top-100 recruiter-ready recommendations
* End-to-end ranking pipeline

---

# Dataset

The system processes approximately **100,000 candidate profiles** provided as part of the Redrob AI Hackathon dataset.

The repository does **not** include the original dataset because it is distributed exclusively for the competition.

---

# Tech Stack

* Python
* Pandas
* NumPy
* Sentence Transformers
* FAISS
* Scikit-learn
* Google Colab

---

# Repository Structure

```
AI-Candidate-Discovery-Ranking/
│
├── notebooks/
│   └── Candidate_Ranking.ipynb
│
├── data/
│   ├── sample_submission.csv
│   └── candidate_schema.json
│
├── outputs/
│   ├── submission_final.csv
│   ├── top100_ranked_final.csv
│   └── candidate_features.csv
│
├── images/
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

---

# How to Run

1. Clone the repository.

```
git clone https://github.com/yourusername/AI-Candidate-Discovery-Ranking.git
```

2. Install dependencies.

```
pip install -r requirements.txt
```

3. Open the notebook.

```
Candidate_Ranking.ipynb
```

4. Run all cells sequentially.

The notebook will:

* Generate candidate features
* Create semantic embeddings
* Retrieve Top-2000 candidates
* Rank candidates using hybrid scoring
* Export the final submission files

---

# Outputs

* candidate_features.csv
* top100_ranked_final.csv
* submission_final.csv

---

# Future Improvements

* Cross-encoder reranking
* LLM-based reasoning for recruiter explanations
* Streamlit recruiter dashboard
* Learning-to-Rank models
* Online feedback loop from recruiter interactions

---

# Author

**Manasvi**

Built for the **Redrob AI Intelligent Candidate Discovery & Ranking Challenge**.
