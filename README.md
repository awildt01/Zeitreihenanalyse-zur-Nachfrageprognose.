# Zeitreihenanalyse-zur-Nachfrageprognose.
  
 [![author](https://img.shields.io/badge/author-wildt-red.svg)](https://www.linkedin.com/in/carlosfab) [![](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/release/python-365/) [![GPLv3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html) [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/carlosfab/data_science/issues)


<p align="center"> 
  <img src="bild/data-analytics-696x464.jpg">       
</p>  

# Alexandre Wildt Graziani 
<sub>*Lead Data Scientist*</sub>




Dieses Projekt zielt darauf ab, ein Vorhersagemodell für die Weinindustrie zu
 entwickeln, um die Bestellmengen basierend auf historischen Verkaufsdaten 
zu optimieren. Dabei wird Facebook Prophet als Zeitreihenmodell genutzt, 
um saisonale Muster und Trends zu erfassen. Zur Optimierung der 
Modellparameter kommt Optuna zum Einsatz, während die Modellgüte mit 
Cross-Validation (Zeitreihen-Validierung) bewertet wird. Die 
Hauptmetriken zur Modellbewertung sind MAPE (Mean Absolute Percentage Error) und MAE (Mean Absolute Error), um 
die Vorhersagegenauigkeit sowohl während der Optimierung als auch auf Testdaten zu messen. 

<br>
<p align=center>
<img src="https://github.com/rafaelnduarte/sigmoidal_data/blob/master/Screen%20Shot%202021-04-01%20at%2012.04.22.png?raw=true" width="70%"></p>
<br/>


**Links:**
* [Notebook](https://nbviewer.org/github/awildt01/Airbnb_Berlin-/blob/main/Airbnb_%28Berlin%29.ipynb)
* [Medium](https://medium.com/@alexandrewildtgraziani/analyse-der-airbnb-berlin-b002125a56f9)
* [Blog](https://sigmoidal.ai)

### Beschaffung der Daten
Alle hier verwendeten Daten wurden von [Rafael Duarte](https://www.linkedin.com/in/rafael-n-duarte/?source=user_about----------------------95e660a7ce9---------------) und Sigmoidal zu verfügung gestellt.

Die Daten sind in zwei Dateien aufgeteilt: eine enthält die historischen Verkaufsdaten, die andere Informationen über die Weine. Beide Dateien wurden in der Cloud gespeichert:

- products.csv - Die Weinkarte, auch die Produkte, ist echt und basiert auf dem tatsächlichen Angebot eines Wein-E-Commerce in den USA. Namen, Jahrgänge und Werte sind zu 100 % authentisch und wurden in US-Dollar umgerechnet, um eine internationale Reichweite zu gewährleisten.
- sales.csv - Dieser Datensatz umfasste ursprünglich 5 Jahre tägliche Verkäufe, verteilt auf 10 Geschäfte, mit einem Katalog von 50 Produkten. Er wurde jedoch geändert und umfasst nun 3 Jahre tägliche Verkäufe, verteilt auf 3 Geschäfte mit 219 verschiedenen Produkten auf Lager.




### Ziel 

Im Wesentlichen entwickelt das Unternehmen eine auf maschinellem Lernen basierende Lösung, um Weinhandlungen dabei zu helfen, ihre Bestände besser zu verwalten. Dazu gehört ein Modell, das die Nachfrage auf der Grundlage historischer Verkaufsdaten prognostiziert.

Ihr spezifischer Bedarf besteht darin, den Teil der Verkaufsprognose zu verfeinern, der die einzigartigen Herausforderungen der Weinwelt und die spezifischen Anforderungen ihres Produkts berücksichtigt.


### Projekt 

Das Ziel das Projekt ist eine explorative Datenanalyse (EDA) durchzuführen. Wir werden die ersten Einblick in der Daten erhalten, Muster identifizieren und Hypothesen aufstellen.
Die folgenden schritt werden in der Analyse durch durchgeführt

Projektschritte

1. Daten laden

Einlesen der Verkaufsdaten aus der bereitgestellten Quelle (CSV, Datenbank etc.).

2. Datenüberblick

Erster Blick auf die Datenstruktur (Anzeigen der ersten Zeilen, Spaltennamen und Datentypen).

Identifikation relevanter Variablen (Datum, Verkaufszahlen, Produktmerkmale etc.).

3. Datenbereinigung

Behandlung fehlender Werte (Imputation oder Entfernung).

Entfernung von Dubletten.

Umgang mit möglichen Ausreißern in den Verkaufszahlen.

4. Transformation der Daten

Umwandlung der Verkaufsdaten in eine stationäre Zeitreihe (falls erforderlich, durch Differenzierung oder logarithmische Transformation).

Erstellung von Dummy-Variablen (One-Hot-Encoding) für kategorische Merkmale wie Feiertage, Produzenten, Länder und Regionen.

Explorative Datenanalyse (EDA)

Berechnung grundlegender statistischer Maße (Durchschnitt, Median, Standardabweichung, Quartile etc.).

Visualisierung der Daten durch Diagramme (Zeitreihenplots, Histogramme, Boxplots etc.).

Untersuchung saisonaler Muster und Trends.

Korrelationsanalyse zwischen den Variablen (z. B. Einfluss von Feiertagen oder Rabatten auf den Umsatz).

Feature Engineering

Einfügen externer Faktoren wie Feiertage, Wetter oder Promotionen als zusätzliche Regressoren für Prophet.

Erstellung zusätzlicher Features basierend auf bisherigen Mustern (z. B. rollierende Mittelwerte, Wochentagseffekte).

Modellentwicklung mit Facebook Prophet

Erstellung des Prophet-Modells mit initialen Parametern.

Einbindung saisonaler Komponenten (jährliche, wöchentliche und tägliche Muster).

Integration externer Regressoren zur Verbesserung der Vorhersagen.

Training des Modells auf historischen Daten.

Hyperparameter-Tuning mit Optuna

Optimierung wichtiger Modellparameter wie changepoint_prior_scale und seasonality_prior_scale.

Nutzung einer zielgerichteten Suche nach den besten Parametern basierend auf den Evaluationsmetriken (MAPE, MAE).

Cross-Validation zur Modellauswertung

Anwendung der Zeitreihen-Cross-Validation zur robusten Bewertung der Modellgüte.

Vergleich der Vorhersagen mit den tatsächlichen Verkaufszahlen.

Identifikation möglicher Overfitting-Probleme.

Ergebnisse und Interpretation

Visualisierung der Prognoseergebnisse.

Berechnung und Bewertung der Modellmetriken (MAPE, MAE, RMSE).

Analyse der saisonalen Effekte und Einflussfaktoren.

Modellbereitstellung und Empfehlung

Erstellung eines Dashboards oder einer API für die Prognosen.

Ableitung von Handlungsempfehlungen basierend auf den Analyseergebnissen.

Bewertung der Vorhersagequalität und mögliche Anpassungen für eine bessere Zukunftsprognose.








### Analysis 


Basierend auf den Ergebnissen der Prognose und der Bewertung können wir Empfehlungen für die Bestandsverwaltung ableiten:

+ Bestverkaufte Produkte des Geschäfts und deren Anteil am Geschäftserfolg.
+ Bestandsoptimierung: Anpassung der Bestellmengen basierend auf den prognostizierten Verkäufen.
+ Rentabilität pro Bestellung, durchschnittliche Versandkosten und durchschnittlicher Betrag, den Kunden ausgeben.
+ Wie beeinflussen verschiedene Monate und Jahreszeiten Ihre Verkäufe?
+ Saisonale Anpassungen: Erhöhung des Bestands in Zeiten mit hoher Nachfrage.
+ Lagerverwaltung: Verbesserung der Lagerverwaltung, um Engpässe zu vermeiden.
+ Welche Artikel brauchen länger, um verkauft zu werden?
+ Wie verhält sich die aktuelle Nachfrage im Vergleich zu früheren Perioden?
+ Bestverkaufte Produkte des Geschäfts und deren Anteil am Geschäftserfolg.


**Background in:** Python, Machine Learning and Mathematical Optimisation.




### Insight


### Projetos:
Veja os tutoriais publicados do Sigmoidal:

* **Visualisierung von Daten aus der Fußball-Bundesliga 2011-2012:** http://bit.ly/3Smgnsn
* **Como Implementar Regressão Linear com Python:** https://bit.ly/2Li5pzY
* **Data Science: Investigando o naufrágio do Titanic:** https://bit.ly/2Ubr5SH
* **Como Tratar Dados Ausentes com Pandas:** https://bit.ly/31KWSMN
* **XGBoost: aprenda este algoritmo de Machine Learning em Python:** https://bit.ly/2UbRhws
* **Como criar uma Wordcloud em Python:** https://bit.ly/2OxsphM
* **Como lidar com dados desbalanceados:** https://bit.ly/2ZlaNsV

---
