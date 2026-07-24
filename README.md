# sentence2vec

Testing theories of sentence vectors on real world data.

## Overview

This repository contains small, self-contained Python examples for building sentence vectors from word vectors and evaluating them on real-world text. The examples focus on:
- Plain average of word vectors
- Weighted average of word vectors
- “Tough to Beat” baseline (SIF-style weighting) for sentence embeddings

Tweets data samples and word-frequency files are provided to demonstrate the methods.

## Project structure

- plain average of word vectors example/
  - sen2vec_plain_average_word_vectors.py
  - tweets.json
- weighed average of word vectors example copy/
  - sen2vec_weighed_average_word_vectors.py
  - tweets.json
  - words-frequency.txt
- tough to beat baseline/
  - sen2vec_weighed_tough_to_beat_baseline.py
  - tweets.json
  - words-frequency.txt
  - temp.txt
- LICENSE
- README.md
- .gitignore

## Requirements

The examples are written for Python 2 and use:
- spaCy (model loaded with name: en)
- requests
- scipy
- scikit-learn
- unidecode
- numpy

Standard library modules used include: json, csv, re, random.

Note:
- The plain average example calls spacy.load('en'), which requires an English model to be installed for your spaCy version.

## Data

- tweets.json files are included with each example to build sentence vectors on real text.
- Some examples reference words-frequency.txt for weighting.
- The plain average example contains an optional Quora evaluation that expects a file at ../quora_duplicate_questions.tsv (not included).

## Usage

Run each example from within its own directory so that local data files (e.g., tweets.json) are found.

- Plain average of word vectors:
  ```
  cd "plain average of word vectors example"
  python sen2vec_plain_average_word_vectors.py
  ```

  Notes:
  - By default, the script loads tweets from the local tweets.json.
  - The Quora evaluation routine in this script expects a TSV file at ../quora_duplicate_questions.tsv if you choose to run it.

- Weighted average of word vectors:
  ```
  cd "weighed average of word vectors example copy"
  python sen2vec_weighed_average_word_vectors.py
  ```

- “Tough to Beat” baseline:
  ```
  cd "tough to beat baseline"
  python sen2vec_weighed_tough_to_beat_baseline.py
  ```

## License

MIT License. See LICENSE for details.
