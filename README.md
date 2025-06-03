# Retrieval-Augmented Generation (RAG) Multi-domain Research System

This repository hosts the implementation of a **Retrieval-Augmented Generation (RAG)** based system designed to assist researchers in analyzing, interpreting, and generating hypotheses from complex literature across diverse domains, including Sikh historical texts, engineering manuals, and scientific papers.

A focused initiative within this larger project is dedicated specifically to developing a highly accurate translation and explanatory commentary (**English Exegesis**) for the Sikh historical manuscript **Naveen Panth Prakash** by Giani Gian Singh, employing advanced OCR and NLP techniques.

---

## Project Goals

### Broad Project (RAG Multi-domain Research System):
- Develop a robust, modular RAG system for supporting scholarly research across multiple fields.
- Enable precise retrieval and generative summarization or hypothesis generation from diverse literature.
- Foster collaboration through open-source contributions and comprehensive documentation.

### Specific Initiative (Naveen Panth Prakash Exegesis):
- Digitize and accurately process historical Gurmukhi manuscripts.
- Provide an English translation with comprehensive explanatory commentary for Naveen Panth Prakash.
- Innovate OCR techniques tailored to historical and complex Gurmukhi scripts, extending upon Mistral OCR.

---

## Project Structure
```bash
rag-multidomain-research/
├── data/                       # Corpus datasets (history, engineering, science)
├── docs/                       # Documentation, reports, papers
├── exegesis-npp/               # Specific sub-project for Naveen Panth Prakash
│   ├── ocr/                    # OCR scripts and model training for Gurmukhi
│   ├── llm/                    # Language models for translation/exegesis
│   └── rag/                    # Specialized retrieval system for Sikh history
├── rag-engineering/            # Engineering literature retrieval
├── rag-science/                # Scientific literature retrieval
├── shared-components/          # Reusable RAG modules and infrastructure
├── app/                        # Frontend/backend applications
├── notebooks/                  # Experimental notebooks
├── tests/                      # Tests for validation and CI
├── LICENSE                     # Open-source license
└── README.md                   # Project overview (this file)
```

---

## Tech Stack

| Component          | Tools & Frameworks                                           |
|--------------------|---------------------------------------------------------------|
| **OCR**            | Tesseract OCR, OpenCV, PyMuPDF, Mistral OCR                   |
| **Language NLP**   | Hugging Face Transformers, Indic NLP, SpaCy, NLTK             |
| **RAG**            | FAISS, Milvus, LangChain, Sentence Transformers               |
| **Deployment**     | Docker, FastAPI, Streamlit, AWS/Azure                         |

---

## Getting Started

### Prerequisites
- Python ≥3.10
- CUDA-enabled GPU recommended
- Docker recommended for reproducibility

### Installation
Clone the repository:
```bash
git clone https://github.com/JaskaranSingh2/rag-multidomain-research.git
cd rag-multidomain-research
```
Setup environment:
```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Usage Examples

OCR Gurmukhi Manuscripts

```bash
python exegesis-npp/ocr/extract.py --input path/to/manuscript.pdf --output output/text.json
```
Generate Exegesis (English Commentary)

```bash
python exegesis-npp/llm/generate_exegesis.py --input output/text.json --output output/exegesis.json
```
Multi-domain Knowledge Retrieval
Retrieve context from domain-specific literature:
```bash
# Sikh History
python exegesis-npp/rag/retrieve.py --query "Battle of Chamkaur"

# Engineering domain
python rag-engineering/retrieve.py --query "Pros and cons of RISC-V architecture"

# Scientific literature
python rag-science/retrieve.py --query "Latest findings in quantum entanglement"
```

Extensions & Future Work

	•	Extend multilingual capabilities for broader accessibility.
	•	Implement automated knowledge discovery and hypothesis generation tools.
	•	Develop interactive knowledge graphs from textual data.

Ethical Considerations & Data Governance (still working on this front...)

	•	We prioritize accurate representation and cultural sensitivity, especially for religious or historical manuscripts.
	•	All data use complies with public domain status or appropriate licensing.
 
License

This project is open-sourced under the MIT License. See LICENSE for details.
