# Model predykcji śmiertelności pacjentów z niewydolnością serca

## Opis projektu

Projekt dotyczy przewidywania ryzyka zgonu pacjentów z niewydolnością serca przy użyciu metod uczenia maszynowego.  
Celem było stworzenie modeli, które przewidują, czy pacjent zmarł (`DEATH_EVENT = 1`) czy przeżył (`DEATH_EVENT = 0`) w okresie obserwacji.  
Szczególną uwagę poświęcono metryce recall, ponieważ w kontekście medycznym najważniejsze jest wykrycie pacjentów zagrożonych zgonem.

## Źródło danych

W projekcie wykorzystano dane z publicznego zbioru [Heart Failure Clinical Records Dataset](https://www.kaggle.com/datasets/andrewmvd/heart-failure-clinical-data), zawierającego informacje o 299 pacjentach. Dane obejmują:

- wiek, płeć  
- frakcję wyrzutową serca  
- poziom kreatyniny, płytek krwi  
- występowanie cukrzycy, nadciśnienia  
- status przeżycia  

## Wykorzystane metody

W projekcie zastosowano następujące algorytmy:

- Regresja logistyczna  
- Drzewa decyzyjne  
- Random Forest  
- SVM (Support Vector Machine)

Dane zostały odpowiednio przeskalowane, podzielone na zbiory treningowe i testowe oraz zbadane wizualnie.  
W ramach analizy porównano skuteczność modeli osobno dla klasy „Zmarł” i „Przeżył”.

## Wyniki modeli

| Model               | Dokł. trening (%) | Dokł. test (%) | CV (5-fold) (%) | F1-score (Zmarł) | Recall (Zmarł) | Uwagi                            |
|---------------------|------------------|----------------|------------------|------------------|----------------|----------------------------------|
| **Regresja logistyczna** | 83.26            | 80.00         | 77.25            | 0.73             | 0.64           | Dobrze zbalansowany model        |
| **SVM**                 | 84.52            | 80.00         | 79.92            | 0.74             | 0.68           | Solidny, stabilny                |
| **Random Forest**       | 92.89            | 73.33         | 84.61            | 0.60             | 0.48           | Przeuczony (overfitting)         |
| **Decision Tree**       | 91.21            | 68.33         | 81.18            | 0.56             | 0.48           | Najsłabszy na danych testowych   |

## Podsumowanie

Najlepsze wyniki osiągnęły modele regresji logistycznej oraz SVM, które zapewniły wysoką jakość predykcji przy jednocześnie zrównoważonych metrykach.  
Modele drzewiaste, mimo wysokiej dokładności na treningu, wykazały tendencję do przeuczenia (overfitting), co ograniczyło ich skuteczność na danych testowych.

---
