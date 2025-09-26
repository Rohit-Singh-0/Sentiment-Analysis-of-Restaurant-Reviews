Sentiment Analysis of Restaurant Reviews
========================================

Classify restaurant reviews as **positive** or **negative** using Natural Language Processing (NLP) and a Naive Bayes classifier.

Project Overview
----------------

*   Preprocesses 1,000 text reviews (cleaning, stopword removal, stemming).
    
*   Converts text into numerical features with Bag-of-Words.
    
*   Trains a Gaussian Naive Bayes classifier.
    
*   Evaluates model with accuracy and confusion matrix.
    

This project demonstrates an end-to-end supervised text classification pipeline in Python.

Dataset
-------

*   File: Restaurant\_Reviews.tsv
    
*   Size: 1,000 reviews with binary sentiment labels (Liked = 1, Not Liked = 0).
    
*   Format: Tab-separated, two columns: Review, Liked.
    

Workflow
--------

1.  **Data Cleaning**
    
    *   Regex filtering of non-alphabet characters.
        
    *   Lowercasing, tokenization, and stopword removal (kept "not").
        
    *   Stemming using Porter Stemmer.
        
2.  **Feature Engineering**
    
    *   Bag-of-Words (CountVectorizer, max 1,500 features).
        
3.  **Model Training**
    
    *   Train/test split (80/20).
        
    *   Gaussian Naive Bayes classifier.
        
4.  **Evaluation**
    
    *   Confusion matrix: printed in notebook.
        
    *   Accuracy score: ~**73%** (from the default run).
        

Results
-------

*   Model: **Gaussian Naive Bayes**
    
*   Test Accuracy: ~**73%**
    
*   \[\[55 42\] \[12 91\]\]
    
*   Strength: Fast and interpretable baseline model.
    
*   Weakness: Bag-of-Words + GaussianNB is limited for complex text patterns.
    

Skills Demonstrated
-------------------

*   Text preprocessing with **NLTK**.
    
*   Feature engineering with **scikit-learn**.
    
*   Supervised learning with **Naive Bayes**.
    
*   Evaluation with confusion matrix and accuracy.
    
*   Jupyter Notebook workflow.
    

Installation
------------

`   git clone https://github.com/Rohit-Singh-0/Sentiment-Analysis-of-Restaurant-Reviews.git  cd Sentiment-Analysis-of-Restaurant-Reviews  python -m venv venv  source venv/bin/activate   # Linux/Mac  # venv\Scripts\activate    # Windows  pip install -r requirements.txt  jupyter notebook Restaurant_Reviews_NLP.ipynb   `

If requirements.txt is missing, install manually:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   pip install numpy pandas matplotlib scikit-learn nltk   `

Next Steps
----------

*   Try **Multinomial Naive Bayes** (better for word counts).
    
*   Experiment with **TF-IDF** features.
    
*   Benchmark advanced models (Logistic Regression, SVM, RandomForest).
    
*   Deploy a simple prediction API or Streamlit app.
