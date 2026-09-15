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

### Running it

The notebook uses only the Python standard library — no third-party packages are needed.

```bash
git clone https://github.com/zainulwahaj/NLP-lab.git
cd NLP-lab
jupyter notebook Lab01_Python_Essentials_for_NLP.ipynb
```

Then run all cells with **Cell → Run All**, or just open the file on GitHub to read the
saved outputs.
