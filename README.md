# TED Talks Search & Recommendation

Individual information-retrieval coursework by **Mengxuan Shen** (Xi'an Jiaotong-Liverpool University).

**Portfolio page with live in-browser demo:** https://shine574269.github.io/projects/ted-retrieval.html

A search engine and "more like this" recommender for 2,550 TED and TEDx talks.

## What it does
- Cleans and combines each talk's title, description and tags.
- Builds a 5,000-feature unigram/bigram TF-IDF index (scikit-learn).
- Ranks talks against a free-text query by cosine similarity, then recommends similar talks for any selected result.
- Tkinter desktop GUI for searching and browsing.

**Evaluation** ("education creativity" query): Precision@5 = 0.80, Precision@10 = 0.60, Recall@10 = 0.75. Main limitation: synonyms are not matched.

## Files
| File | Contents |
|---|---|
| `ted_retrieval_system.py` | Indexing, search, recommendation and evaluation |
| `gui_demo.py` | Tkinter desktop interface |
| `dataset.csv` | TED talk metadata used by the system |
| `original-source-and-data.zip` | Original coursework source and data as submitted |

## Running
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
python gui_demo.py
```

## Credits
Talk titles, descriptions and links © TED Conferences, LLC (ted.com), used here for non-commercial coursework.
