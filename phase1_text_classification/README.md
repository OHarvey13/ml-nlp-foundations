## Notes - This README.md is strictly for my notes. It may be unorganized for viewers

### Libraries 
    - CountVectorizer (BoW): converts text into a matrix of word counts — basically, how often each word appears in each document.
    - TfidfVectorizer: converts text into a weighted matrix that considers both word frequency and how rare the word is across all documents. Rare but important words get higher weight.
    -Why needed: Machine learning models can’t understand raw text, they need numbers.

    - Note for README:
    - BoW = counts only (simple)
    - TF-IDF = counts weighted by importance (better for distinguishing documents)
    - MultinomialNB (Naive Bayes):
        - Probabilistic model.
        - Assumes each word occurs independently given the class.
        - Good for text classification because it works with word counts (multinomial distribution).
        - Fast and works well even if the independence assumption is not true.
    -Logistic Regression:
        - Linear model that predicts the probability of each class.
        - Optimizes cross-entropy loss.
        - Works well with high-dimensional sparse data (like TF-IDF).
    Tip: Think Naive Bayes = fast & simple, Logistic Regression = slightly more flexible & powerful.