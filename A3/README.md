<h1>Harmonizing Knowledge Graphs and Deep Learning</h1>
  <p><strong>Author:</strong> Betzalel Moskowitz<br>
     <strong>Course:</strong> MSDS453-DL: Natural Language Processing<br>
     <strong>Date:</strong> November 27, 2023</p>

  <h2>Overview</h2>
  <p>
    This project explores two parallel tracks—knowledge graph (KG) construction and deep learning (DL) modeling—using movie review data. The goal is to uncover business insights and improve information extraction processes through refined entity-relationship modeling and sequential language understanding.
  </p>

  <h2>Project Structure</h2>
  <ul>
    <li><code>Dereferenced_Assignment3.csv</code> – Output of initial pronoun resolution and dereferencing of entities from raw movie reviews</li>
    <li><code>Dereferenced_Assignment3_v2.csv</code> – A refined version of the dereferenced dataset, featuring cleaned, normalized entities and improved mapping to ontology terms</li>
    <li><code>Moskowitz_Assignment3.pdf</code> – Final project paper detailing methodology, experiments, results, and analysis across both the knowledge graph and deep learning components</li>
    <li><code>Notebooks/</code> – Jupyter notebooks supporting both the knowledge graph and deep learning components:
      <ul>
        <li><code>dereference_pronouns_from_class_corpus.ipynb</code> – Uses OpenAI API to resolve pronouns and map them to canonical entities</li>
        <li><code>MSDS453_Assignment_03_SUP00_v03_20231025_KnowledgeGraphs.ipynb</code> – Constructs and visualizes the initial knowledge graph</li>
        <li><code>MSDS453_Assignment_03_SUP00_v03_20231025_KnowledgeGraphs_OpenAI.ipynb</code> – Expanded KG with dereferenced inputs using OpenAI</li>
        <li><code>MSDS453_Assignment_03_LSTM_32_32.ipynb</code> – BiLSTM model with two 32-unit dense layers for genre/sentiment classification</li>
        <li><code>MSDS453_Assignment_03_LSTM_32_32_Dropout.ipynb</code> – Same architecture as above, with dropout regularization added</li>
        <li><code>MSDS453_Assignment_03_LSTM_32_Dropout.ipynb</code> – Simpler model with one 32-unit dense layer and dropout</li>
        <li><code>MSDS453_Assignment_03_LSTM_64.ipynb</code> – BiLSTM model with a 64-unit dense layer (no dropout)</li>
        <li><code>MSDS453_Assignment_03_LSTM_64_64.ipynb</code> – Two 64-unit dense layers, larger architecture for comparison</li>
        <li><code>MSDS453_Assignment_03_LSTM_64_Dropout.ipynb</code> – Same as above but with dropout to prevent overfitting</li>
      </ul>
    </li>
    <li><code>html/</code> – Offline HTML exports of all Jupyter notebooks from the <code>Notebooks/</code> directory for easy viewing and sharing without requiring a Jupyter environment</li>
  </ul>

  <h2>Knowledge Graph Construction</h2>
  <p>
    The knowledge graph was constructed from a small corpus of 10 movie reviews of the film <em>Equilibrium</em>, using spaCy for POS tagging and triplet extraction. Enhancements included:
  </p>
  <ul>
    <li>Pronoun resolution using the OpenAI Chat Completion API</li>
    <li>Manual normalization of equivalent terms (e.g., “john” and “preston” → “john preston”)</li>
  </ul>
  <p>
    Graphs were visualized using <code>networkx</code> to compare entity frequencies and relationships across stages of refinement.
  </p>

  <h2>Deep Learning Experiments</h2>
  <p>
    The second part of the project involves training BiLSTM models to classify:
  </p>
  <ul>
    <li><strong>Sentiment:</strong> Positive vs. negative reviews</li>
    <li><strong>Genre:</strong> Action, Comedy, Horror, or Sci-Fi</li>
  </ul>
  <p>
    Reviews were preprocessed (tokenized, cleaned, stopword removed, lemmatized) and vectorized using a <code>TextVectorization</code> layer. Various dense layer configurations were evaluated for performance.
  </p>

  <h2>Key Results</h2>
  <ul>
    <li><strong>Knowledge Graph:</strong> Final graph reduced redundancy and better matched the initial ontology; limitations remain in modeling opinion-based or implicit knowledge.</li>
    <li><strong>Sentiment Classification:</strong> Best model: 32-unit single dense layer without dropout; 72% test accuracy.</li>
    <li><strong>Genre Classification:</strong> Best model: 32-unit dense layer with 10% dropout; 83% test accuracy.</li>
  </ul>

  <h2>Insights</h2>
  <ul>
    <li>Pronoun and entity resolution significantly improved KG coherence but required manual effort.</li>
    <li>Smaller DL models outperformed larger ones, likely due to limited data.</li>
    <li>LSTMs provided benefits for sentiment tasks (due to sequence sensitivity), but genre classification was competitive with classic ML on small datasets.</li>
  </ul>

  <h2>Future Work</h2>
  <ul>
    <li>Experiment with automatic triplet extraction via generative LLMs for improved KG coverage</li>
    <li>Expand dataset size to unlock full potential of deep learning architectures</li>
    <li>Develop scalable, semi-automated pipelines for term normalization and entity linking</li>
  </ul>

  <h2>Requirements</h2>
  <ul>
    <li>Python 3.8+</li>
    <li>Libraries: <code>spaCy, networkx, nltk, keras, tensorflow, pandas, openai</code></li>
    <li>OpenAI API key for pronoun resolution (KG component)</li>
  </ul>

  <h2>License</h2>
  <p>This project was developed as part of coursework for educational purposes.</p>

  <h2>Citations</h2>
  <p>
    If you wish to cite this work, please use the following citation:<br>
    <blockquote>
      Moskowitz, B. (2023). <em>Harmonizing Knowledge Graphs and Deep Learning: Unraveling Business Insights from Movie Reviews</em>. MSDS453-DL: Natural Language Processing. Northwestern University.
    </blockquote>
  </p>
