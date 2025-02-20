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

Die Daten sind in zwei Dateien aufgeteilt: eine enthält die historischen Verkaufsdaten, die andere Informationen über die Weine. Beide Dateien wurden in der Cloud gespeichert, falls sie nicht verfügbar sind oder Änderungen in der Zukunft vorgenommen werden. Diese gespeicherten Dateien werden im Code verwendet, um die Integrität der Studie zu gewährleisten.:

- products.csv - Die Weinkarte, auch die Produkte, ist echt und basiert auf dem tatsächlichen Angebot eines Wein-E-Commerce in den USA. Namen, Jahrgänge und Werte sind zu 100 % authentisch und wurden in US-Dollar umgerechnet, um eine internationale Reichweite zu gewährleisten.
- sales.csv - Dieser Datensatz umfasste ursprünglich 5 Jahre tägliche Verkäufe, verteilt auf 10 Geschäfte, mit einem Katalog von 50 Produkten. Er wurde jedoch geändert und umfasst nun 3 Jahre tägliche Verkäufe, verteilt auf 3 Geschäfte mit 219 verschiedenen Produkten auf Lager.




### Ziel 

Im Wesentlichen entwickelt das Unternehmen eine auf maschinellem Lernen basierende Lösung, um Weinhandlungen dabei zu helfen, ihre Bestände besser zu verwalten. Dazu gehört ein Modell, das die Nachfrage auf der Grundlage historischer Verkaufsdaten prognostiziert.

Ihr spezifischer Bedarf besteht darin, den Teil der Verkaufsprognose zu verfeinern, der die einzigartigen Herausforderungen der Weinwelt und die spezifischen Anforderungen ihres Produkts berücksichtigt.


### Projekt 

Das Ziel das Projekt ist eine explorative Datenanalyse (EDA) durchzuführen. Wir werden die ersten Einblick in der Daten erhalten, Muster identifizieren und Hypothesen aufstellen.
Die folgenden schritt werden in der Analyse durch durchgeführt

1. Data Laden 

2. Datenüberblick: Ersten Blick auf die Daten, um deren Struktur und Größe zu verstehen. Anzeigen der ersten Zeilen, Spaltennamen und Datentypen.

3. Datenbereinigung: Identifizieren und behandeln von fehlende Werte, Dubletten oder Ausreißer.

4. Deskriptive Statistiken: Berechnung grundlegender statistischer Maße wie Durchschnitt, Median, Standardabweichung und Quartile, um ein besseres Verständnis der Verteilung der Daten zu erhalten.
  
5. Datenvisualisierung: Erstellung vom Diagramme, Grafiken und Plots, um die Verteilung und Beziehungen zwischen den Variablen zu visualisieren.

6. Korrelationsanalyse: Untersuchung von Korrelationen zwischen verschiedenen Variablen, um festzustellen, ob starke Beziehungen vorhanden sind.

7. Hypothesenbildung: Auf der Grundlage von Beobachtungen und Analysen werden angenommen, wie verschiedene Faktoren miteinander in Beziehung stehen






### Analysis 


Folgende Fragen werde ich durch der Analyse  beantworten:

+ Die ursprüngliche Idee von Airbnb bestand darin, ein Zimmer oder ein Mehrbettzimmer im eigenen Zuhause anzubieten. Ist das immer noch so?
+ Welche Art von Immobilien wird auf Airbnb am häufigsten vermietet?
+ Sind die Angebote gleichmäßig über die Stadtteile verteilt oder gibt es Hotspots?
+ Welcher Viertel ist im Datensatz am teuersten?
+ Was ist der Durchschnittspreis für Mieten?
+ Welcher Host hat die meisten Anzeigen?
+ Was ist der Durchschnitt der Mindestaufenthaltsdauer für Mietwohnungen (minimum_nights)?
+ Sind Immobilien im Besitz einzelner Nutzer oder gibt es Nutzer mit mehreren Mietobjekten (d. h. potenziell für Spekulationen)?


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
