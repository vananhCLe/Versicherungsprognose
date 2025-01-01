# Versicherungsgebührenanalyse und -vorhersage

## Projektübersicht

Dieses Projekt umfasst die Analyse und Vorhersage von Versicherungsgebühren mit Python. Der Datensatz enthält Details wie Alter, Geschlecht, BMI, Anzahl der Kinder, Rauchstatus, Region und Gebühren. Ziel ist es, Erkenntnisse aus den Daten zu gewinnen und Versicherungskosten basierend auf Schlüsselfaktoren vorherzusagen.

## Inhaltsverzeichnis

1. Datensatzübersicht
2. Verwendete Technologien
3. Datenanalyse
4. Datenvorverarbeitung
5. Modellentwicklung
6. Erkenntnisse
7. Ergebnisse

### 1. Datensatzübersicht

Wir werden mit einem Datensatz von Kaggle arbeiten: 
* Medical Cost Personal Datasets: Sie können mehr darüber lesen [here](https://www.kaggle.com/datasets/mirichoi0218/insurance)

Der Datensatz enthält 1.338 Einträge mit den folgenden Spalten:

* age: Alter der versicherten Person
* sex: Geschlecht (männlich/weiblich)
* bmi: Body-Mass-Index
* children: Anzahl der unter der Versicherung abgedeckten Kinder
* smoker: Rauchstatus (ja/nein)
* region: Wohnregion (Südost, Südwest, Nordost, Nordwest)
* charges: Medizinische Gebühren, die von der Krankenversicherung in Rechnung gestellt werden

Im Datensatz wurden keine fehlenden Werte festgestellt.

### 2. Verwendete Technologien

* Programmiersprache: Python
* Bibliotheke:
   * numpy
   * pandas
   * matplotlib
   * seaborn
   * sklearn
  
### 3. Datenanalyse

#### Statistische Erkenntnisse

* Das Alter der Personen liegt zwischen 18 und 64 Jahren.
* Die BMI-Werte liegen zwischen 15 und 53, mit einer leicht rechtsschiefen Verteilung.
* 50 % der Personen haben keine Kinder, während nur circa 1 % 4 oder 5 Kinder haben.
* Raucher machen 20 % des Datensatzes aus, während Nichtraucher 80 % ausmachen.

#### Visualisierungen

1. Altersverteilung: Die meisten Personen sind zwischen 18 und 22 Jahre alt.
2. BMI-Verteilung: Leicht rechtsschief mit einigen Ausreißern.
3. Gebühren nach Rauchstatus: Raucher zahlen deutlich höhere Gebühren (Median ≈ 35.000 vs. ≈ 7.500 für Nichtraucher).
4. Gebühren nach Region: Die Gebühren sind relativ gleichmäßig über die Regionen verteilt, mit einigen Ausreißern.

### 4. Datenvorverarbeitung

* Kodierung kategorischer Merkmale:
  * sex: männlich (0), weiblich (1)
  * smoker: ja (0), nein (1)
  * region: Südost (0), Südwest (1), Nordost (2), Nordwest (3)
    
* Merkmale für die Vorhersage:
  * Eingabe: age, sex, bmi, children, smoker, region
  * Zielvariable: charges

### 5. Modellentwicklung

* Verwendetes Modell: Lineare Regression
* Prozess:

  1. Aufteilen der Daten in Trainings- (80 %) und Testdaten (20 %) mit train_test_split.
  2. Trainieren des Modells mit den Trainingsdaten.
  3. Bewertung mit Metriken wie Mean Absolute Error (MAE) und R-squared-Wert.
     
### 6. Erkenntnisse

6.1. Schlüsselfaktoren, die die Gebühren beeinflussen:
   * Der Rauchstatus hat den größten Einfluss auf die Gebühren.
   * Der Rauchstatus hat den größten Einfluss auf die Gebühren.
6.2. Einfluss der Region: Regionen zeigen keine signifikanten Unterschiede bei den Gebühren.

### 7. Ergebnisse

* Modellleistung:
   * R-squared-Wert: 0.751505643411174
   * Mean Absolute Error (MAE): 0.7447273869684077
     
* Vorhersagebeispiel:
   * Eingabe: Alter = 31, BMI = 25,74, Geschlecht = Female, Kinder:0, Raucher: nein, Region = southeast
   * Vorhergesagte Gebühren: 3760.08

## Zukünftige Verbesserungen

1. Einbeziehen zusätzlicher Merkmale wie medizinischer Vorgeschichte oder Lebensstil-Daten.
2. Einsatz fortgeschrittener Modelle (z. B. Random Forest, Gradient Boosting) für genauere Vorhersagen.
3. Optimierung der Hyperparameter zur Verbesserung der Genauigkeit.



     

