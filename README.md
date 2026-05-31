# Klasyfikacja wydolności fizycznej

Projekt klasyfikacji poziomu sprawności fizycznej (klasy A/B/C/D) 
na podstawie parametrów antropometrycznych i wydolnościowych.  
Zrealizowany w ramach studiów podyplomowych **Uczenie Maszynowe 
i Data Science** — Uniwersytet Ekonomiczny w Katowicach (2025).

---

## Problem

Przewidywanie klasy wydolności fizycznej osoby (A = najwyższa, 
D = najniższa) na podstawie cech:

| Cecha | Opis |
|---|---|
| age | Wiek |
| gender | Płeć |
| height_cm | Wzrost (cm) |
| weight_kg | Waga (kg) |
| body fat_% | Procent tkanki tłuszczowej |
| gripForce | Siła chwytu |
| sit and bend forward_cm | Gibkość |
| sit-ups counts | Liczba pompek |
| broad jump_cm | Długość skoku w dal |
| class | **Etykieta decyzyjna (A/B/C/D)** |

Źródło danych: [Kaggle — Body Performance Data](https://www.kaggle.com/datasets/kukuroo3/body-performance-data)

---

## Wyniki

Porównano 9 algorytmów klasyfikacyjnych. Kryterium wyboru: recall (macro).

| Model | Accuracy | Recall (macro) | F1 (macro) |
|---|---|---|---|
| Decision Tree (domyślny) | ~% | ~% | ~% |
| Decision Tree (max_depth=10) | ~% | ~% | ~% |
| Random Forest | ~% | ~% | ~% |
| **SVM ← najlepszy** | **~%** | **~%** | **~%** |
| Gradient Boosting | ~% | ~% | ~% |
| KNN | ~% | ~% | ~% |
| Naive Bayes | ~% | ~% | ~% |



Kroswalidacja (cv=10) dla Decision Tree potwierdziła optymalną 
głębokość drzewa na poziomie max_depth = X.

---

## Technologie

- Python 3.x
- pandas, NumPy — przetwarzanie danych
- scikit-learn — modele ML, kroswalidacja, metryki
- matplotlib — wizualizacja
