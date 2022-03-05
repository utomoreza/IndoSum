# Description
===========

This folder contains Indonesian text summarization dataset,
roughly 19K tokenized news articles from (formerly) Shortir.com,
a news aggregator site. The dataset is split into 5 cross-validation
folds, where each fold consists of a training set, a development set,
and a test set. The filenames have the following format (where X is
a fold number 1-5):

* train.0X.jsonl - training set for fold X
* dev.0X.jsonl - development set for fold X
* test.0X.jsonl - test set for fold X

Each file is in JSONL format, where each line is a JSON object corresponding
to an article. This JSON object has several keys:

* id - unique identifier of the article
* paragraphs - a list of paragraphs of the original article
* summary - gold summary of the article, given as a list of sentences
* gold_labels - gold extractive labels of the sentences in the article
* category - category to which the article belongs (in Indonesian)
* source - source of the article
* source_url - url of the original article

A paragraph is given as a list of sentences. A sentence is given as a list
of words. A word is given as a string token.

# License
=======

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0
International License. See http://creativecommons.org/licenses/by-sa/4.0/.

# Citation
========

If you're using our code or dataset, please cite:

@inproceedings{kurniawan2018,
  place={Bandung, Indonesia},
  title={IndoSum: A New Benchmark Dataset for Indonesian Text Summarization},
  url={https://ieeexplore.ieee.org/document/8629109},
  DOI={10.1109/IALP.2018.8629109},
  booktitle={2018 International Conference on Asian Language Processing (IALP)},
  publisher={IEEE},
  author={Kurniawan, Kemal and Louvan, Samuel},
  year={2018},
  month={Nov},
  pages={215-220}
}
