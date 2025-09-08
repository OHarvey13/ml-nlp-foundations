## Notes - This README.md is strictly for my notes. It may be unorganized for viewers

💡 Memory tip: Think D → S → V → M → E → R when coding. Say it out loud while recalling the library/functions for each step.
| Step             | Purpose                     | Library / Function                                   | Notes / Memory Tip                                                                   |
| ---------------- | --------------------------- | ---------------------------------------------------- | ------------------------------------------------------------------------------------ |
| **D: Dataset**   | Load data & labels          | `sklearn.datasets.fetch_20newsgroups`                | `data` = text, `target` = numeric labels, `target_names` = human-readable categories |
| **S: Split**     | Train/test split            | `train_test_split`                                   | Prevent overfitting; `test_size=0.2`, set `random_state` for reproducibility         |
| **V: Vectorize** | Convert text → numbers      | `CountVectorizer`, `TfidfVectorizer`                 | BoW = counts; TF-IDF = weighted; `fit_transform` on train, `transform` on test       |
| **M: Model**     | Train classifiers           | `MultinomialNB`, `LogisticRegression(max_iter=1000)` | NB = fast & simple; LR = flexible & works well with TF-IDF                           |
| **E: Evaluate**  | Check performance           | `accuracy_score`, `classification_report`            | Look at accuracy, precision, recall, F1 for each class                               |
| **R: Reflect**   | Learn & observe limitations | N/A                                                  | BoW/TF-IDF ignore word order; NB ignores dependencies; sets baseline for neural nets |

What does test_size=0.2 mean?  
- This is taking only 20% of the data to be testing with, reserving it.

Why is it important to have a train/test split?
- so the model can learn from itself, and the data its working with. also so we can confirm the model is working. Overfitting is the act of the model memorizing the data.  

Why set a random_state?
- keeps the randomness of the split fixed.


What’s the difference between fit_transform and transform? 
 - one fits the data to match the training set and the other transforms the test
 - fit_transform
   - Learns the vocabulary from the training data and transforms the text into vectors.
 - transform
   - Learns the vocabulary from the training data and transforms the text into vectors.
 - Fit = learn, Transform = convert. Fit + transform together = learn + convert on training data. 

How does TF-IDF weigh words differently than BoW? 
 - BoW: counts each word equally, no matter how common.
 - TF-IDF: adjusts counts by importance:
 - TF (Term Frequency): how often a word appears in a document
 - IDF (Inverse Document Frequency): reduces the weight of words that appear in many documents
 - Result: Common words like “computer” that appear everywhere get lower weight; distinctive words get higher weight.
 - Memory tip: TF-IDF = “counts × importance.”

Why do we remove stop words?
 - stop words account for conjuction words, such as and, the, is, etc. These words hold little to no weight in the classification process.
 - removing them reduces the noise and size of the feature matrix 