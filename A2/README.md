<h1>Topic Modeling and Classification of Political Speech</h1>

  <p><strong>Author:</strong> Betzalel Moskowitz<br>
     <strong>Course:</strong> MSDS453-DL: Natural Language Processing<br>
     <strong>Date:</strong> November 6, 2023</p>

  <h2>Overview</h2>
  <p>
    This project investigates how topic modeling and document embeddings can support political speech classification.
    Using a corpus of inaugural addresses by U.S. presidents, the project explores the efficacy of traditional TF-IDF
    methods and Doc2Vec-based embeddings in both unsupervised (topic modeling, clustering) and supervised (classification)
    settings. The goal is to understand the evolving themes in political language and to evaluate how well different
    representations support genre-based prediction.
  </p>

  <h2>Project Structure</h2>
  <ul>
    <li><code>Notebooks/</code> – Jupyter notebooks used for each stage of analysis:
      <ul>
        <li><code>MSDS453_Assignment_02_TF_IDF_Classification.ipynb</code> – Logistic regression classifier using TF-IDF features</li>
        <li><code>MSDS453_Assignment_02_Clustering_TF-IDF.ipynb</code> – K-Means clustering on TF-IDF vectors</li>
        <li><code>MSDS453_Assignment_02_Topic_Modeling_2_topics.ipynb</code> – LDA topic modeling with 2 topics, visualizing word distributions</li>
        <li><code>MSDS453_Assignment_02_Clustering_Doc2Vec_100.ipynb</code> – K-Means clustering on Doc2Vec embeddings (100 dimensions)</li>
        <li><code>MSDS453_Assignment_02_Clustering_Doc2Vec_200.ipynb</code> – Same as above with 200-dimensional vectors</li>
        <li><code>MSDS453_Assignment_02_Clustering_Doc2Vec_300.ipynb</code> – Same as above with 300-dimensional vectors</li>
        <li><code>MSDS453_Assignment_Doc2Vec_100_Classification.ipynb</code> – Logistic regression classifier on 100-dimensional Doc2Vec embeddings</li>
        <li><code>MSDS453_Assignment_Doc2Vec_500_Classification.ipynb</code> – Same as above with 500-dimensional vectors</li>
        <li><code>MSDS453_Assignment_Doc2Vec_1000_Classification.ipynb</code> – Same as above with 1000-dimensional vectors</li>
      </ul>
    </li>
    <li><code>html/</code> – Offline HTML exports of all notebooks for convenient viewing outside a Jupyter environment</li>
    <li><code>Moskowitz_Assignment2.pdf</code> – Final project paper describing motivation, methods, results, and conclusions</li>
  </ul>

  <h2>Methods</h2>
  <p>
    The project is structured in three stages:
    <ol>
      <li><strong>Exploratory Analysis & Topic Modeling:</strong> Using LDA to identify major themes in political speeches</li>
      <li><strong>Unsupervised Clustering:</strong> Applying K-Means to TF-IDF and Doc2Vec vectors to explore document groupings</li>
      <li><strong>Supervised Classification:</strong> Predicting whether a speech was given pre- or post-1950 using both TF-IDF and Doc2Vec representations</li>
    </ol>
  </p>

  <h2>Key Findings</h2>
  <ul>
    <li>LDA topics successfully surfaced interpretable themes such as "freedom/peace" vs. "government/economy"</li>
    <li>Clustering on Doc2Vec vectors yielded more stable groupings than TF-IDF due to better semantic generalization</li>
    <li>Classification accuracy improved with higher dimensional Doc2Vec embeddings, peaking at 1000 dimensions</li>
    <li>TF-IDF models performed strongly but lacked the transferability of embedding-based models</li>
  </ul>

  <h2>Requirements</h2>
  <ul>
    <li>Python 3.8+</li>
    <li>Libraries: <code>nltk, gensim, scikit-learn, pandas, matplotlib, seaborn</code></li>
  </ul>

  <h2>License</h2>
  <p>This project was developed as part of coursework for educational purposes.</p>

  <h2>Citations</h2>
  <p>
    If you wish to cite this work, please use the following citation:<br>
    <blockquote>
      Moskowitz, B. (2023). <em>Topic Modeling and Classification of Political Speech</em>. MSDS453-DL: Natural Language Processing. Northwestern University.
    </blockquote>
  </p>
