<h1>Topic Modeling and Classification of Movie Reviews</h1>

  <p><strong>Author:</strong> Betzalel Moskowitz<br>
     <strong>Course:</strong> MSDS453-DL: Natural Language Processing<br>
     <strong>Date:</strong> November 6, 2023</p>

  <h2>Overview</h2>
  <p>
    This project investigates how topic modeling and vector representations can support classification of movie reviews by sentiment and genre. Using a subset of reviews from Rotten Tomatoes and IMDb, we apply unsupervised and supervised techniques to discover latent structure and evaluate predictive models. Both traditional vectorizers (TF-IDF) and neural embeddings (Doc2Vec) are explored for document representation.
  </p>

  <h2>Project Structure</h2>
  <ul>
    <li><code>Notebooks/</code> – Jupyter notebooks used for modeling:
      <ul>
        <li><code>MSDS453_Assignment_02_TF_IDF_Classification.ipynb</code> – Logistic regression classifier using TF-IDF features</li>
        <li><code>MSDS453_Assignment_02_Clustering_TF-IDF.ipynb</code> – K-Means clustering on TF-IDF vectors to group reviews</li>
        <li><code>MSDS453_Assignment_02_Topic_Modeling_2_topics.ipynb</code> – LDA topic modeling on review corpus (2 topics)</li>
        <li><code>MSDS453_Assignment_02_Clustering_Doc2Vec_100.ipynb</code> – K-Means clustering using Doc2Vec (100 dimensions)</li>
        <li><code>MSDS453_Assignment_02_Clustering_Doc2Vec_200.ipynb</code> – Same as above using 200 dimensions</li>
        <li><code>MSDS453_Assignment_02_Clustering_Doc2Vec_300.ipynb</code> – Same as above using 300 dimensions</li>
        <li><code>MSDS453_Assignment_Doc2Vec_100_Classification.ipynb</code> – Doc2Vec + logistic regression for sentiment/genre classification (100 dim)</li>
        <li><code>MSDS453_Assignment_Doc2Vec_500_Classification.ipynb</code> – Same as above (500 dimensions)</li>
        <li><code>MSDS453_Assignment_Doc2Vec_1000_Classification.ipynb</code> – Same as above (1000 dimensions)</li>
      </ul>
    </li>
    <li><code>html/</code> – HTML exports of all notebooks for offline viewing</li>
    <li><code>Moskowitz_Assignment2.pdf</code> – Final project paper with methodology, experiments, analysis, and conclusions</li>
  </ul>

  <h2>Methods</h2>
  <ol>
    <li><strong>Topic Modeling:</strong> LDA used to surface latent themes (e.g., emotional vs. action-based tone)</li>
    <li><strong>Clustering:</strong> TF-IDF and Doc2Vec features clustered using K-Means to explore review groupings</li>
    <li><strong>Classification:</strong> Logistic regression models built to predict:
      <ul>
        <li><strong>Sentiment:</strong> Positive or negative</li>
        <li><strong>Genre:</strong> Action, Comedy, Horror, Sci-Fi</li>
      </ul>
    </li>
  </ol>

  <h2>Key Findings</h2>
  <ul>
    <li>LDA was effective at splitting reviews into interpretable themes (e.g., plot vs. emotion)</li>
    <li>Doc2Vec features improved clustering coherence and classification accuracy compared to TF-IDF</li>
    <li>Higher-dimensional embeddings (500–1000) led to stronger classification results, especially for sentiment</li>
    <li>TF-IDF worked well with logistic regression but lacked semantic richness</li>
  </ul>

  <h2>Requirements</h2>
  <ul>
    <li>Python 3.8+</li>
    <li>Libraries: <code>nltk, gensim, scikit-learn, pandas, matplotlib, seaborn</code></li>
  </ul>

  <h2>License</h2>
  <p>This project was developed for educational purposes as part of a graduate-level NLP course.</p>

  <h2>Citations</h2>
  <p>
    If you wish to cite this work, please use the following citation:<br>
    <blockquote>
      Moskowitz, B. (2023). <em>Topic Modeling and Classification of Movie Reviews</em>. MSDS453-DL: Natural Language Processing. Northwestern University.
    </blockquote>
  </p>
