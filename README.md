# NLP Lab

Lab work for the **Natural Language Processing** course.

| | |
|---|---|
| **Name** | Zain Ul Wahaj |
| **Roll Number** | FA23-BAI-058 |
| **Course** | Natural Language Processing |

---

## Lab 01 — Python Essentials for NLP

[`Lab01_Python_Essentials_for_NLP.ipynb`](Lab01_Python_Essentials_for_NLP.ipynb)

A complete, fully executed solution to all **9 tasks (36 parts)** of Lab 01. Every
lettered part is solved in its own code cell, placed directly under the question it
answers, with its output saved in the notebook — so the results are visible on GitHub
without running anything.

### Tasks

| # | Task | Topic |
|---|------|-------|
| 01 | Strings as Text Storage | String (`str`) |
| 02 | Lists for Token Management | List (`list`) |
| 03 | Dictionaries for Word Mapping | Dictionary (`dict`) |
| 04 | Sets for Unique Vocabulary | Set (`set`) |
| 05 | Tuples for Fixed Linguistic Data | Tuple (`tuple`) |
| 06 | String Cleaning Methods | `lower`, `upper`, `strip`, `split`, `join`, `replace` |
| 07 | String Validation Methods | `find`, `startswith`, `endswith`, `isdigit`, `isalpha` |
| 08 | Functions and Lambda for NLP Pipelines | Functions, lambda |
| 09 | `map()`, `filter()`, `sorted()` and Counter | `map`, `filter`, `sorted`, `collections.Counter` |

### Topics covered

- The five core Python data structures from an NLP perspective — storing sentences,
  managing tokens, mapping words to IDs and frequencies, building unique vocabularies,
  and holding fixed linguistic pairs such as POS tags.
- String methods for cleaning and validating raw text before further processing.
- Reusable text-processing pipelines built from functions and lambdas.
- Functional tools (`map`, `filter`, `sorted`) and frequency counting with `Counter`.

---

## Lab 02 — PDF, DOCX and REST API Data Extraction

[`Lab02_PDF_DOCX_and_API_Data_Extraction.ipynb`](Lab02_PDF_DOCX_and_API_Data_Extraction.ipynb)

All **9 tasks (36 parts)**, fully executed with saved outputs.

| # | Task | Topic |
|---|------|-------|
| 01 | Multi-Page PDF Extraction with Word Frequency Analysis | `pdfplumber`, `re.sub`, word frequencies, keyword search with `input()` |
| 02 | Structured Page Metadata Extraction and CSV Export | per-page dictionaries, custom `PhraseNotFoundError`, `csv` module |
| 03 | PDF Text Preprocessing Pipeline for NLP | cleaning with `re.sub`, sentence splitting, NLTK stop words |
| 04 | DOCX Paragraph Classification and Statistical Analysis | `python-docx`, paragraph styles, nested dictionaries |
| 05 | DOCX Table Extraction and Pandas Integration | `doc.tables`, DataFrames, walking `doc.element.body` |
| 06 | Multi-Document Comparison, Deduplication, and Frequency Report | set operations, `Counter` |
| 07 | Multi-Endpoint API Data Joining and Analysis | `requests`, joining users and posts |
| 08 | To-Do Completion Rate Analysis Across Users | validation, grouping, formatted tables |
| 09 | Nested JSON Flattening, DataFrame Operations, and Comment Analysis | `flatten_user`, pandas, `math.sqrt` |

**Input files** are in [`data/`](data): `sample_nlp.pdf` (8 pages, page 4 is blank on purpose so the
zero-word case is exercised), `report_a.docx` (headings, body text, bullets, blank paragraphs and two
tables) and `report_b.docx` (overlaps with report A). The notebook also writes `pdf_summary.csv`,
`nlp_ready_output.txt` and `docx_extracted.txt`; the copies in this repository are the ones it produced.

**About the saved outputs.** Tasks 01 (d) and 02 (c) ask for keyboard input; the saved outputs used the
answers `language` and `machine learning`. Tasks 07-09 call https://jsonplaceholder.typicode.com. That
site could not be reached from the environment where the saved outputs were produced, so they were
generated against a local server that serves the same dataset (the public `typicode/jsonplaceholder`
`data.json`) at the same URLs. Running the notebook with internet access uses the live API.

## Lab 03 — Regex and Tokenization with NLTK and spaCy

[`Lab03_Regex_and_Tokenization.ipynb`](Lab03_Regex_and_Tokenization.ipynb)

All **5 tasks (20 parts)**, fully executed.

| # | Task | Topic |
|---|------|-------|
| 01 | Regex Fundamentals | `\d`, capital-letter words, exactly four digits, 3-6 letter words |
| 02 | Pattern-Based Extraction | emails, `03XX-XXXXXXX` phone numbers, `DD/MM/YYYY` dates, percentages |
| 03 | Word Tokenization (NLTK vs spaCy) | `word_tokenize()` vs a blank spaCy pipeline, differences found |
| 04 | Token Attributes | `is_alpha`, `like_num`, `like_email`, `is_currency` |
| 05 | Sentence Segmentation | `en_core_web_sm`, `doc.sents`, abbreviations |

NLTK and spaCy tokenize contractions, abbreviations and URLs the same way, but differ on quotation marks
(NLTK rewrites `"` as two backquotes / two apostrophes) and on hyphenated words (spaCy splits them).

## Lab 04 — Text Preprocessing and Edit Distance

[`Lab04_Text_Preprocessing_and_Edit_Distance.ipynb`](Lab04_Text_Preprocessing_and_Edit_Distance.ipynb)

All **9 tasks (36 parts)**, fully executed.

| # | Task | Topic |
|---|------|-------|
| 01 | Lowercasing Basics and Its Drawbacks | vocabulary before/after, ambiguous cases (US/us, Apple/apple) |
| 02 | Noise Removal Pipeline | one regex function per noise type, effect of ordering, over-cleaning |
| 03 | Stop-Word Removal and Its Effect on Vocabulary | NLTK stop words, movie reviews, custom list |
| 04 | Risks of Stop-Word Removal | negation and sentiment, Urdu translation, chatbot intent, safe strategy |
| 05 | Hands-On with the Porter Stemmer | correct/incorrect table, over- and under-stemming, Snowball |
| 06 | Lemmatization (spaCy) vs. Stemming | token / POS / stem / lemma table, speed comparison |
| 07 | Preprocessing Pipeline | configurable class, four configurations, TF-IDF + Logistic Regression |
| 08 | Implementing Minimum Edit Distance | recursive, dynamic programming, backtrace, substitution cost 2 |
| 09 | Spelling Correction with Edit Distance | Brown-corpus dictionary, Top-1 accuracy, frequency tie-break |

Some results worth knowing: removing stop words flipped the sentiment of 4 of 5 negated sentences;
stemming was about 18x faster than lemmatization; all four preprocessing configurations scored about
0.77-0.78 accuracy (differences are smaller than the fold-to-fold spread); spaCy lemmatized `better` as
`well` and `hoping` as `hop`; and the frequency tie-break did not improve spelling-correction accuracy
(85% both ways). The Urdu translations in Task 04 call the public Google Translate web endpoint, so
they need an internet connection and may change slightly over time.

## Lab 05 — N-gram Language Models

[`Lab05_Ngram_Language_Models.ipynb`](Lab05_Ngram_Language_Models.ipynb)

All **9 tasks (36 parts)**, standard library only, natural logarithm, values rounded to 4 decimals.

| # | Task | Topic |
|---|------|-------|
| 01 | Tokenization | `tokenize()` with `<s>` / `</s>`, `build_vocab()` (V = 11) |
| 02 | Generating N-grams | `get_ngrams()`, the m - n + 1 rule, n larger than the sentence |
| 03 | Counting N-grams | `Counter` tables, `count_of()` for unseen n-grams |
| 04 | Unigram model | MLE, probabilities sum to 1, word order does not matter |
| 05 | Bigram model (MLE) | chain rule, next-word distribution, `predict_next()` |
| 06 | Trigram model | trigram sentence probability, unseen n-grams |
| 07 | Zero-probability problem | unseen bigrams, 87% of word pairs never seen, `safe_log()` |
| 08 | Smoothing | add-one and add-k |
| 09 | Perplexity and model comparison | model table, best k, tuning on a validation sentence |

The first test sentence has bigram probability 0.0156 and trigram probability 0.125; the second contains
the unseen bigram `fish sat`, so its MLE probability is 0 and its perplexity is infinite until smoothing is applied.

---

## Requirements

| Lab | Needs |
|---|---|
| 01 | Python standard library only |
| 02 | `pdfplumber`, `python-docx`, `pandas`, `requests`, `nltk` |
| 03 | `nltk`, `spacy` with the `en_core_web_sm` model |
| 04 | `nltk`, `spacy` (`en_core_web_sm`), `pandas`, `matplotlib`, `scikit-learn`, `requests` |
| 05 | Python standard library only |

```bash
pip install pdfplumber python-docx pandas requests nltk spacy matplotlib scikit-learn
python -m spacy download en_core_web_sm
```

NLTK data (`punkt_tab`, `stopwords`, `movie_reviews`, `brown`) is downloaded automatically by the notebooks when missing.

## Running

```bash
git clone https://github.com/zainulwahaj/NLP-lab.git
cd NLP-lab
jupyter notebook
```

Open any notebook and run all cells with **Cell → Run All**, or just open the file on GitHub to read the
saved outputs. Run the notebooks from the repository root so that the `data/` paths resolve.
