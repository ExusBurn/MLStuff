# Project Report: Clinical Word2Vec Embeddings

###  Objective
To train a Word2Vec model on clinical text data and visualize the learned word embeddings, revealing semantic relationships between medical terms.

---

###  Dataset
- **Type:** Synthetic clinical discharge notes
- **Size:** 10 manually written entries, each simulating realistic scenarios (e.g., chest pain, headache, infections)

---

###  Preprocessing
- Lowercased all text
- Tokenized using regex-based tokenizer (due to `nltk` issues)
- Removed common English stopwords
- Kept only alphabetic tokens

---

###  Model Training
- **Library:** Gensim’s `Word2Vec`
- **Algorithm:** Skip-Gram (`sg=1`)
- **Vector Size:** 100
- **Context Window:** 5
- **Min Count:** 1
- Model trained on the preprocessed tokenized notes

---

###  Visualization
- Used **PCA** to reduce high-dimensional vectors (100D → 2D)
- Plotted using Matplotlib
- Words with related meanings formed visible clusters (e.g., symptoms grouped together)

---

###  Conclusion
The Word2Vec model learned meaningful semantic relationships even from a small corpus of synthetic clinical notes. Visualizations showed that symptom-related and treatment-related terms clustered well, highlighting the strength of unsupervised word embeddings in capturing context. This workflow can be extended to real clinical corpora and integrated into downstream tasks such as classification, clustering, or clinical decision support.

---

###  Tools Used
- Python 3.10+
- Gensim
- scikit-learn (PCA)
- Matplotlib
- Jupyter Notebook (VSCode)

---

###  Final Thoughts
This project provided hands-on experience with NLP preprocessing, unsupervised learning, and vector space visualization. It's a foundation for more advanced clinical NLP systems using real-world data.

