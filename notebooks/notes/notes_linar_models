# Linear Models – Summary (SVM, SGD, SVR)

This repository contains notes and implementations related to **linear models**, including classification and regression using Support Vector Machines (SVM), Gradient Descent, and Support Vector Regression (SVR).

---

## 🔹 1. Linear SVM Classifier

- Learns a decision boundary that maximizes the margin between two classes.
- Margin = distance between the hyperplane and closest data points.
- Uses **hinge loss**: `max(0, 1 - t * (wᵀx + b))`
- Objective: minimize `0.5 * ||w||² + C * loss`
- `C` controls the trade-off between margin width and training error.

---

## 🔹 2. Gradient Descent Variants

| Type         | Description              | Pros           | Cons                     |
|--------------|--------------------------|----------------|--------------------------|
| Batch GD     | Uses all data            | Stable         | Slow on large datasets   |
| Stochastic GD| One sample at a time     | Fast, scalable | Noisy, less stable       |
| Mini-Batch   | Small batch (e.g. 32)    | Best of both   | Requires tuning batch size|

---

## 🔹 3. Custom SVM – `MyLinearSVC`

- Implements batch gradient descent on hinge loss.
- Tracks loss (`self.Js`) at each epoch.
- Identifies support vectors (points with margin < 1).
- Methods:
  - `.fit(X, y)`: training loop
  - `.predict(X)`: returns class 0 or 1
  - `.decision_function(X)`: raw decision score

---

## 🔹 4. Comparison with scikit-learn models

| Model              | Solver             | Uses GD | Notes                        |
|--------------------|--------------------|---------|------------------------------|
| `LinearSVC`        | LibLinear          | ❌      | Fast, for small datasets     |
| `SVC(kernel='linear')` | SMO             | ❌      | Works with kernels           |
| `SGDClassifier`    | Stochastic GD      | ✅      | Scalable, customizable       |
| `MyLinearSVC`      | Batch GD           | ✅      | Educational purpose          |

---

## 🔹 5. SVR (Support Vector Regression)

- Predicts continuous output.
- Uses epsilon-insensitive loss:  
  No penalty if prediction is within ±ε.
- `C`: penalizes margin violations.
- `ε`: defines the width of the no-penalty tube.

---

## 🔹 6. Hinge vs Squared Hinge Loss

| Type              | Formula              | Effect                          |
|-------------------|-----------------------|----------------------------------|
| Hinge Loss        | `max(0, 1 - t * s)`   | Linear penalty                  |
| Squared Hinge     | `(max(0, 1 - t * s))²`| Stronger penalty on misclassified |

---

## 🔹 7. Key Concepts

- All models learn: `f(x) = wᵀx + b`
- Training = minimizing regularized loss
- Margin and loss controlled via `C`, `epsilon`
- Support vectors define decision boundary
- Visualization of decision boundaries helps understanding

---

## 🔹 8. Recommendations

- Use `SGDClassifier(loss='hinge')` for large datasets and manual tuning.
- Use `LinearSVC` for efficient, clean SVM classification.
- Always visualize the decision boundary and the convergence of your model.
