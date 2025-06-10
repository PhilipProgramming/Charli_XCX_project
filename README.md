# Charli_XCX_project
lyrical analysis 

# Charli XCX Lyrics Analysis & Semantic Clustering

This project explores the lyrics of Charli XCX using Natural Language Processing (NLP) techniques to uncover thematic patterns, stylistic changes, and song groupings. The analysis includes traditional word frequency metrics, semantic embeddings, and unsupervised clustering to visualize lyrical trends across her discography.

## 📂 Project Structure

- `updated_lyrics.csv`: Raw dataset of Charli XCX lyrics with track titles, disc labels, and full lyrics.
- `charli_project.ipynb`: Main notebook performing all analyses (preprocessing, vectorization, clustering, and visualization).
- `semantic_report_hdbscan.png`: Final cluster visualization using HDBSCAN and BERT embeddings.
- `emotion_by_disc`: Bar Graph of sentiment by disc.
- `tf_idf_and_random_forest`: Additional metrics from Random Forest classifier.

## 🧠 Methods Used

### 🔤 Text Preprocessing
- Lowercasing, stopword removal, and lemmatization using `spaCy`.
- Bag-of-Words and TF-IDF vectorization to capture lexical features.

### 🧪 Word Analysis
- Chi-square test for top disc-specific words.
- Word frequency and presence analysis to highlight thematic language per album/disc.

### 📊 Classification
- Random Forest classifier trained to distinguish between Disc 1 and Disc 2 songs using TF-IDF features.
- Evaluation using `precision`, `recall`, and `f1-score`.

### 🌌 Semantic Clustering
- Sentence-BERT embeddings (`all-MiniLM-L6-v2`) to represent song lyrics semantically.
- UMAP for 2D dimensionality reduction.
- HDBSCAN for unsupervised clustering to group semantically similar songs.
- K-Means applied to the HDBSCAN noise cluster (`-1`) to uncover weaker thematic groupings.

## 🖼️ Visualizations

- **K-Means Clustering on Word Frequency** – Grouped songs based on surface-level lexical similarity.
- **HDBSCAN Semantic Clustering** – Captured deeper song similarities using embeddings.
- **Noise Cluster Subclustering** – Used K-Means to reveal structure within the outliers from HDBSCAN.

## 📈 Results Summary

- Disc 1 and Disc 2 exhibit statistically distinct word usage patterns.
- The Random Forest classifier struggled with generalization due to the small dataset.
- BERT-based clustering produced more meaningful thematic groupings than TF-IDF.
- HDBSCAN effectively filtered noise songs, which were further split using K-Means into coherent subgroups.

## 🚀 Technologies Used

- Python
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn`, `hdbscan`, `umap-learn`
- `sentence-transformers` for semantic embeddings

## 📌 Future Directions

- Expand dataset with more albums or artists for comparative analysis.
- Integrate lyrical metadata (genre, tempo, popularity).
- Build a recommendation engine using lyric similarity.

## 📝 Acknowledgments

Lyrics data sourced for academic and illustrative purposes. All credit to Charli XCX and respective rights holders.

---

