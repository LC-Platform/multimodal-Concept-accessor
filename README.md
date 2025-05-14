# Keyword Extraction Techniques in Python

This project explores and compares six different keyword extraction techniques implemented in a Jupyter notebook. The goal is to extract meaningful keywords from scientific or general text using a variety of NLP methods.

##  Notebook Overview

The notebook implements and evaluates the following **six approaches** to keyword extraction:

---

##  1. TF-IDF Variants

TF-IDF (Term Frequency-Inverse Document Frequency) is a classic statistical method used to evaluate how important a word is to a document.

The following variations are explored:

- **Without Threshold**  
  Direct TF-IDF application, extracting top `n` terms.

- **With Threshold**  
  Filters out keywords with low TF-IDF scores (e.g., below 0.1).

- **With POS Tagging**  
  Uses POS (Part-of-Speech) filtering to retain only relevant types (e.g., nouns, adjectives).

- **With Lemmatization**  
  Converts words to their root forms (e.g., "studies" → "study").

- **With Threshold Adjustment**  
  Dynamically adjusts thresholds based on score distribution or document characteristics.

---

##  2. SpaCy + SciSpaCy (SciBERT Model)

Uses:
- [`spaCy`](https://spacy.io/)
- [`scispaCy`](https://allenai.github.io/scispacy/)
- `en_core_sci_scibert` model

This approach leverages a domain-specific transformer model trained on scientific text to extract **named entities** and domain-specific keywords.

---

##  3. KeyBERT

Uses:
- KeyBERT
KeyBERT generates keywords by embedding both the document and candidate phrases using a BERT-based model, and then selecting keywords that are semantically similar to the document.

---

## 4. YAKE

Uses:
- yake

Yet Another Keyword Extractor (YAKE) is a lightweight unsupervised method that uses statistical features from the text itself (like casing, position, frequency) without external corpora.

---

##  5. RAKE

Uses:
- rake-nltk

RAKE (Rapid Automatic Keyword Extraction) is an unsupervised, domain-independent keyword extraction algorithm based on the frequency of co-occurring words.

---

##  6. RAKE-NLTK

A variant of RAKE integrated with NLTK, using improved tokenization, stopword handling, and better phrase extraction.

---

##  Example Input

You can provide input as raw scientific or general text. Each method will process the text and output the most relevant keywords.

---

##  Output

Each method returns a list of keywords. You can compare:

* Keyword quality
* Semantic similarity
* Length and relevance
* Domain specificity (e.g., scientific vs general text)

---


