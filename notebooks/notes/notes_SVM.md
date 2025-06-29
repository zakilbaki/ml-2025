## 🔍 SVM Notes – Rappels Clés

- SVM ne se contente pas de séparer les données, il **les sépare avec la plus grande marge possible**, ce qui améliore la **robustesse au bruit** et la **généralisation**.
- Le **scaling est crucial** avec les SVM (ex: `StandardScaler`) car ils sont **sensibles aux échelles**.
- **SVM est très sensible aux outliers**.

---

### ✅ Interprétation des scores
- Si `score > 0` → prédiction = classe 1 (positif)
- Plus le score est **éloigné de 0**, plus le modèle est **confiant**.

---

### 🎯 Influence du paramètre `C`
- `C=100`: essaie de parfaitement séparer les données → marge étroite, **risque de surapprentissage**.
- `C=1`: accepte quelques erreurs → marge plus large, **meilleure généralisation**.

---

### 🌀 SVM Non Linéaire et Kernels
- Un **SVM non linéaire** est un SVM qui utilise le **kernel trick** pour apprendre des **frontières courbes**.
- Le **kernel polynomial** permet de projeter implicitement les données dans un espace de plus grande dimension.
- Le **kernel RBF** (Gaussian) utilise des **landmarks** et calcule des **similarités** entre chaque point et les landmarks → permet de bien séparer dans l’espace projeté.

> Le kernel trick permet de **calculer des produits scalaires dans un espace de dimension supérieure sans y aller explicitement**.

---

### 📈 SVR (Support Vector Regression)
- Version régression du SVM.
- Essaie de prédire une fonction **plate** qui reste dans un **tube d’erreur ±ε**.
- `C` → contrôle la pénalité pour les grosses erreurs.
- `ε` → définit ce qu’est une erreur tolérable.
- Très utile pour gérer les **outliers sans les supprimer**.

---

### 💥 Squared Hinge Loss
- `hinge = max(0, 1 - t*s)`  
- `squared_hinge = (max(0, 1 - t*s))²`
- La squared hinge loss **pénalise plus fortement** les erreurs → peut aider à mieux apprendre.

---

### ⚙️ Gradient Descent et SVM
| Modèle                        | Utilise Gradient Descent ? | Optimiseur                     |
|------------------------------|-----------------------------|--------------------------------|
| `LinearSVC`                  | ❌                          | Coordinate Descent (LibLinear) |
| `SVC(kernel=...)`            | ❌                          | SMO (LibSVM)                   |
| `SGDClassifier(loss='hinge')`| ✅                          | Stochastic Gradient Descent    |

> ✅ `SGDClassifier` est **le seul modèle SVM dans sklearn qui utilise le gradient descent.`

---
