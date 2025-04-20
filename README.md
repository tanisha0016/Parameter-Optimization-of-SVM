# Parameter-Optimization-of-SVM
This project explores SVM hyperparameter tuning and compares clustering algorithms (KMeans, MeanShift, Hierarchical) on the Iris dataset using various preprocessing techniques. Performance is evaluated using key clustering metrics and visualized for insights.

# NuSVC Optimization on Iris Dataset

This project performs randomized hyperparameter tuning of the `NuSVC` classifier on the classic Iris dataset. It evaluates model accuracy across different kernel and `nu` parameter combinations, using 10 randomized train-test splits. Results are visualized to understand convergence trends.

---

## Dataset

- **Dataset**: Iris Dataset from `sklearn.datasets`
- **Classes**: 3 (Setosa, Versicolor, Virginica)
- **Features**: 4 numerical features (sepal/petal length and width)

---

##  Methodology

### 1. **Preprocessing**
- Feature scaling with `StandardScaler`.

### 2. **Randomized Optimization**
- Performed over **10 train-test splits** with 30% test size.
- For each split:
  - Run **30 iterations** of model training using randomized hyperparameters.
  - Randomly selected:
    - `kernel` ∈ {linear, rbf, poly, sigmoid}
    - `nu` ∈ [0.01, 0.9]
  - Track best accuracy and parameters.
  - Plot accuracy over iterations to show convergence.

### 3. **Metrics**
- Accuracy score on the test set for each iteration.
- Summary table of best results per split.

---

## 📈 Results Summary

| Sample | Best Accuracy (%) | Best Parameters                |
|--------|-------------------|--------------------------------|
| S1     | 97.78             | {'kernel': 'rbf', 'nu': 0.19}  |
| S2     | 97.78             | {'kernel': 'poly', 'nu': 0.52} |
| S3     | 100.00            | {'kernel': 'linear', 'nu': 0.24} |
| S4     | 95.56             | {'kernel': 'poly', 'nu': 0.32} |
| S5     | 97.78             | {'kernel': 'linear', 'nu': 0.61} |
| S6     | 97.78             | {'kernel': 'linear', 'nu': 0.58} |
| S7     | 97.78             | {'kernel': 'sigmoid', 'nu': 0.54} |
| S8     | 95.56             | {'kernel': 'linear', 'nu': 0.10} |
| S9     | 95.56             | {'kernel': 'poly', 'nu': 0.02} |
| S10    | 100.00            | {'kernel': 'rbf', 'nu': 0.47} |

---


## Conclusion

- NuSVC, with randomized hyperparameter tuning, achieves **up to 100% accuracy** on the Iris dataset.
- Both `linear` and `rbf` kernels frequently emerged as top performers.
- Convergence graphs highlight the variability in performance across different parameter choices and train-test splits.

---

## Future Work

- Integrate more sophisticated tuning methods like **Bayesian Optimization** or **GridSearchCV**.
- Extend analysis to more complex datasets or apply cross-validation for more robust results.
- Compare performance with other models like `SVC`, Decision Trees, or k-NN.

---

## Author

Built by [Tanisha Ahuja] – exploring SVMs, model tuning, and visualization with scikit-learn.

