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
