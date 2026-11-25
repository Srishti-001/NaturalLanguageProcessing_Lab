# Natural Language Processing Lab

This repository contains ten experiments for the Computational Linguistics and Natural Language Processing lab. It brings together Jupyter notebooks, supporting datasets and documents, two applied NLP projects, and the complete lab report.

The experiments progress from text processing and linguistic analysis to word representations, classification, summarization, and machine translation. Experiments 9 and 10 are presented as Project 1 and Project 2, respectively.

**Complete lab report:** [500124490_SrishtiBatham_NLP_Exp1ToExp10_LabReport.pdf](./500124490_SrishtiBatham_NLP_Exp1ToExp10_LabReport.pdf)

## Repository structure

```text
.
|-- 500124490_SrishtiBatham_NLP_Exp1ToExp10_LabReport.pdf
|-- CNLP_Exp1.ipynb
|-- CNLP_Exp2.ipynb
|-- CNLP_Exp3.ipynb
|-- CNLP_Exp4.ipynb
|-- CNLP_Exp5.ipynb
|-- CNLP_Exp6/
|   |-- Experiment_6.ipynb
|   |-- Experiment-6.docx
|   `-- glove_corpus.txt
|-- CNLP_Exp7/
|   |-- Experiment_7.ipynb
|   |-- Experiment_7_v2.ipynb
|   |-- Experiment-7.docx
|   `-- IMDB-Dataset.csv
|-- CNLP_Exp8/
|   |-- experiment-8.ipynb
|   |-- Experiment-8.docx
|   |-- mBERTScore-comparison.png
|   `-- ROUGEScore-comparison.png
|-- CNLP_Exp9(Project1)/
|   |-- app.py
|   |-- nlp_pipeline.py
|   |-- test_pipeline.py
|   |-- requirements.txt
|   |-- README.md
|   |-- DEPLOYMENT.md
|   `-- .venv/ (bundled environment)
|-- CNLP_Exp10(Project2)/
|   |-- app.py
|   |-- nmt.py
|   |-- README.md
|   |-- requirements.txt
|   |-- models/
|   |-- results/
|   |-- static/
|   `-- templates/
`-- CNLP_Exp1toExp5_AdditionalContent/
    |-- Exp1_Content/
    |-- Exp2_Content/
    |-- Exp3_Content/
    |-- Exp4_Content/
    `-- Exp5_Content/
```

The tree shows the main tracked materials; generated caches and the contents of bundled model and environment directories are grouped rather than expanded.

## Experiments

| No. | Experiment | Overview |
|---:|---|---|
| 1 | Employee Data Analysis | Analyze the employee dataset, including departmental salary and headcount summaries and salary, age, gender, and experience visualizations. |
| 2 | Basic Text Preprocessing, Tokenization, and Stopword Removal | Clean and preprocess text, tokenize it, and remove stopwords. |
| 3 | Stemming, Lemmatization, and Regular Expression | Apply stemming, lemmatization, and regular-expression operations to text. |
| 4 | Term Frequency, TF-IDF, and Named Entity Recognition | Calculate term-frequency and TF-IDF values and identify named entities. |
| 5 | Subword-Level Tokenization and POS Tagging | Explore subword tokenization, including BPE, and part-of-speech tagging. |
| 6 | GloVe Word Embeddings and Statistical Language Modelling | Implement and explore GloVe word representations, including word-similarity tasks and statistical language modelling. |
| 7 | Sentiment Classification on the IMDB Movie Reviews Dataset | Compare sentiment-classification approaches, including Logistic Regression and a BERT-based model; the folder contains two notebook versions. |
| 8 | Hindi Abstractive Text Summarization using mT5 and mBART | Fine-tune mT5 and mBART on the Hindi XL-Sum configuration and evaluate summaries with ROUGE and multilingual BERTScore. |
| 9 — Project 1 | 30-Second News Reel Brief Generator | A Streamlit application that turns news content into short reel scripts using NLP processing, TextRank, topic and entity analysis, and evaluation checks. |
| 10 — Project 2 | Low-Resource Neural Machine Translation for Indic Languages using Fine-Tuned NLLB-200 | Fine-tune NLLB-200 for English and Indic language pairs, compare with zero-shot translation, and provide command-line and Flask interfaces. |

### Additional content for Experiments 1–5

`CNLP_Exp1toExp5_AdditionalContent/` contains supplementary practical materials organized by experiment. These include experiment documents, employee and text inputs, sample documents for Experiment 4, and CSV outputs for term-frequency, TF-IDF, and named-entity results.

## Technologies

- **Languages and environments:** Python, Jupyter notebooks, and Google Colab.
- **Notebook libraries:** pandas, NumPy, Matplotlib, seaborn, NLTK, spaCy, scikit-learn, Gensim, Hugging Face `tokenizers` and `transformers`, SentencePiece, PyTorch, Hugging Face `datasets`, tqdm, `rouge-score`, and `bert-score`.
- **Project 1:** Streamlit, feedparser, trafilatura, newspaper3k, spaCy, NLTK, requests, and `rouge-score`.
- **Project 2:** Flask, PyTorch, Transformers, Accelerate, SentencePiece, Hugging Face `datasets`, gdown, pandas, openpyxl, and SacreBLEU. COMET is documented as an optional evaluation metric.
- **Web interface assets:** HTML, CSS, and JavaScript are used by the Experiment 10 Flask application.

Dependencies are experiment-specific; the repository does not provide one root-level environment file for all notebooks.

## Navigating and running the experiments

1. Clone the repository and enter its folder:

   ```bash
   git clone https://github.com/Srishti-001/NaturalLanguageProcessing_Lab.git
   cd NaturalLanguageProcessing_Lab
   ```

2. Open `CNLP_Exp1.ipynb` through `CNLP_Exp5.ipynb` in Jupyter or Google Colab. Open the corresponding notebook inside `CNLP_Exp6/`, `CNLP_Exp7/`, or `CNLP_Exp8/` for the later notebook experiments. Experiment 7 includes two notebook versions. Use the accompanying datasets and supporting content where the notebook requires them; install any missing notebook dependencies in that runtime.

3. Run **Experiment 9 — Project 1** from its folder:

   ```bash
   cd "CNLP_Exp9(Project1)"
   python -m pip install -r requirements.txt
   streamlit run app.py
   ```

   To run its pipeline checks, use `python test_pipeline.py` in the same folder.

4. Return to the repository root (`cd ..`) if needed, then run **Experiment 10 — Project 2** from its folder:

   ```bash
   cd "CNLP_Exp10(Project2)"
   python -m pip install -r requirements.txt
   python nmt.py languages
   python app.py
   ```

   To train the Assamese model using the documented sample limit, run `python nmt.py train --lang as --max-train-samples 20000 --epochs 1`. Training requires a GPU; Google Colab T4 is recommended in the project documentation. The website is available at `http://127.0.0.1:5000` when the Flask application is running. Training downloads its data as described in the Experiment 10 README.

## Author

**Srishti Batham**<br>
B.Tech Computer Science and Engineering (Artificial Intelligence and Machine Learning), Semester VII
