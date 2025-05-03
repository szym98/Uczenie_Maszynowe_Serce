Projekt dotyczy przewidywania ryzyka zgonu pacjentów z niewydolnością serca przy użyciu metod uczenia maszynowego.
Wykorzystano dane z publicznego zbioru Heart Failure Clinical Records Dataset, dostępnego na platformie Kaggle:
 https://www.kaggle.com/datasets/andrewmvd/heart-failure-clinical-data.
 Zbiór zawiera dane kliniczne 299 pacjentów, m.in. wiek, frakcję wyrzutową serca, poziom kreatyniny, płytki krwi, występowanie cukrzycy, nadciśnienia i anemii. 
 Celem projektu było stworzenie modeli, które przewidują, czy pacjent zmarł (DEATH_EVENT = 1) czy przeżył (DEATH_EVENT = 0) w okresie obserwacji. 
 Szczególną uwagę poświęcono metryce recall, ponieważ w kontekście medycznym najważniejsze jest wykrycie pacjentów zagrożonych zgonem.

Zastosowano kilka klasyfikatorów: regresję logistyczną, drzewa decyzyjne, Random Forest, SVM . 
Dane zostały odpowiednio przeskalowane, podzielone na zbiory treningowe i testowe oraz zbadane wizualnie. 
W ramach analizy porównano skuteczność modeli osobno dla klasy „Zmarł” i „Przeżył”. 
