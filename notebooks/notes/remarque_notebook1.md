# 📓 Remarques Notebook 1

Dans ce premier notebook, voici les points les plus importants traités :

1️⃣ **Reproductibilité avec la seed**  
- Lors de l'utilisation de générateurs aléatoires, il est essentiel de fixer la seed (`np.random.seed()`) pour assurer la reproductibilité du code.

2️⃣ **Type de visualisation adapté**  
- Le type de graphique dépend de la nature des variables et de ce que l'on veut observer (scatter plot, courbes, etc.).

3️⃣ **Évaluation des modèles : MSE, RMSE, MAE, R²**  
- Différences et intérêts de chaque métrique pour mesurer les performances de la régression.

4️⃣ **Choix optimal de K en KNN**  
- Utilisation de la validation croisée pour déterminer la meilleure valeur de `k` dans le K-Nearest Neighbors.

5️⃣ **Sauvegarde des plots proprement**  
- Sauvegarde automatique des figures avec `Path()` pour organiser les images de façon reproductible.

6️⃣ **Merge, GroupBy et indexation intelligente**  
- Intérêt de placer une colonne en index (`set_index()`) pour simplifier les jointures et agrégations.

7️⃣ **Mise en valeur de points particuliers dans un scatter plot**  
- Annotations et flèches sur les points d’intérêt pour mieux expliquer visuellement les observations clés.

8️⃣ **Régression polynomiale + standardisation**  
- Importance de standardiser les features polynomiales pour stabiliser l'apprentissage.

9️⃣ **Pipelines Scikit-Learn (💡 très important)**  
- Enchaînement propre des transformations et du modèle dans un objet unique (`Pipeline`) pour automatiser le workflow.

🔟 **Régularisation pour lutter contre l'overfitting**  
- Les termes L1 (Lasso) et L2 (Ridge) permettent de limiter les poids trop grands :
  - L1 : annule certains coefficients (sélection de variables)
  - L2 : pénalise fortement les gros poids sans les annuler.
