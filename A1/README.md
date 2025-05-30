<h1>Data Wrangling and Vectorization Techniques for NLP Clustering</h1>

  <p><strong>Author:</strong> Betzalel Moskowitz<br>
     <strong>Course:</strong> MSDS453-DL: Natural Language Processing<br>
     <strong>Date:</strong> October 31, 2023</p>

  <h2>Overview</h2>
  <p>
    This project explores how different data wrangling strategies and vectorization techniques affect the performance of clustering tasks in NLP.
    Using a collection of movie reviews, the analysis focuses on grouping together reviews about the sci-fi film <em>Equilibrium</em> and similar documents.
    We experiment with TF-IDF, Word2Vec, and Doc2Vec representations across multiple preprocessing strategies and embedding dimensions.
  </p>

  <h2>Project Structure</h2>
  <ul>
    <li><code>Notebooks/</code> – All modeling notebooks used for experiments:
      <ul>
        <li><code>MSDS453_Assignment_01_M1_TF_IDF_100.ipynb</code></li>
        <li><code>MSDS453_Assignment_01_M1_TF_IDF_200.ipynb</code></li>
        <li><code>MSDS453_Assignment_01_M1_TF_IDF_300.ipynb</code></li>
        <li><code>MSDS453_Assignment_01_M2_TF_IDF_100.ipynb</code></li>
        <li><code>MSDS453_Assignment_01_M2_TF_IDF_200.ipynb</code></li>
        <li><code>MSDS453_Assignment_01_M2_TF_IDF_300.ipynb</code></li>
        <li><code>MSDS453_Assignment_01_M3_TF_IDF_100.ipynb</code></li>
        <li><code>MSDS453_Assignment_01_M3_TF_IDF_200.ipynb</code></li>
        <li><code>MSDS453_Assignment_01_M3_TF_IDF_300.ipynb</code></li>
      </ul>
    </li>
    <li><code>html/</code> – HTML exports of the above notebooks for offline viewing</li>
    <li><code>Moskowitz_Assignment1.pdf</code> – Final project report summarizing methodology, results, and analysis</li>
  </ul>

  <h2>Methods</h2>
  <ol>
    <li><strong>Data Wrangling Techniques:</strong> Three tiers of preprocessing:
      <ul>
        <li><strong>M1:</strong> Tokenization + normalization</li>
        <li><strong>M2:</strong> M1 + lemmatization + stop word removal</li>
        <li><strong>M3:</strong> M2 + non-alphabetic token removal + custom stop word filtering</li>
      </ul>
    </li>
    <li><strong>Vectorization Approaches:</strong>
      <ul>
        <li><strong>TF-IDF:</strong> Sparse term-document matrix using scikit-learn</li>
        <li><strong>Word2Vec:</strong> Dense embeddings trained using Gensim</li>
        <li><strong>Doc2Vec:</strong> Paragraph vector model for full-document embeddings</li>
      </ul>
    </li>
    <li><strong>Embedding Dimensions Tested:</strong> 100, 200, and 300</li>
    <li><strong>Evaluation Metrics:</strong> Cosine similarity, clustering heatmaps, hierarchical clustering, and t-SNE plots</li>
  </ol>

  <h2>Key Findings</h2>
  <ul>
    <li>Data wrangling had the largest impact on clustering quality—particularly lemmatization and stop word removal (M2 and M3)</li>
    <li>TF-IDF was effective at clustering documents discussing the same movie (e.g., <em>Equilibrium</em>)</li>
    <li>Word2Vec successfully grouped similar terms and confirmed the importance of manually identified prevalent terms</li>
    <li>Doc2Vec underperformed in this context, possibly due to small dataset size</li>
    <li>Higher embedding dimensions (up to 300) yielded slight improvements but were secondary to preprocessing gains</li>
  </ul>

  <h2>Requirements</h2>
  <ul>
    <li>Python 3.8+</li>
    <li>Libraries: <code>nltk, gensim, scikit-learn, pandas, matplotlib, seaborn</code></li>
  </ul>

  <h2>License</h2>
  <p>This project is for educational use and was completed as part of a graduate course at Northwestern University.</p>

  <h2>Citations</h2>
  <p>
    If you would like to cite this project or its findings, please use:<br>
    <blockquote>
      Moskowitz, B. (2023). <em>Data Wrangling and Vectorization Techniques for NLP Clustering</em>. MSDS453-DL: Natural Language Processing. Northwestern University.
    </blockquote>
  </p>
