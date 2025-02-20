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
* [Notebook]()
* [Medium](https://medium.com/@alexandrewildtgraziani/analyse-der-airbnb-berlin-b002125a56f9)
* [Blog](https://sigmoidal.ai)

### Beschaffung der Daten
Alle hier verwendeten Daten wurden von [Rafael Duarte](https://www.linkedin.com/in/rafael-n-duarte/?source=user_about----------------------95e660a7ce9---------------) und Sigmoidal zu verfügung gestellt.

Die Daten sind in zwei Dateien aufgeteilt: eine enthält die historischen Verkaufsdaten, die andere Informationen über die Weine. Beide Dateien wurden in der Cloud gespeichert:

- products.csv – Weinkarte eines Wein-E-Commerce. Die Weinkarte sowie die darin enthaltenen Produkte basieren auf dem tatsächlichen Sortiment eines Wein-E-Commerce in den USA. Namen, Jahrgänge und Preise sind vollständig authentisch und wurden in US-Dollar umgerechnet, um eine internationale Vergleichbarkeit und Reichweite zu ermögliche
- sales.csv - Dieser Datensatz umfasste ursprünglich 5 Jahre tägliche Verkäufe, verteilt auf 10 Geschäfte, mit einem Katalog von 50 Produkten. Er wurde jedoch geändert und umfasst nun 3 Jahre tägliche Verkäufe, verteilt auf 3 Geschäfte mit 219 verschiedenen Produkten auf Lager.


<br>

### Ziel 

Im Wesentlichen entwickelt das Unternehmen eine auf maschinellem Lernen basierende Lösung, um Weinhandlungen dabei zu helfen, ihre Bestände besser zu verwalten. Dazu gehört ein Modell, das die Nachfrage auf der Grundlage historischer Verkaufsdaten prognostiziert.

Ihr spezifischer Bedarf besteht darin, den Teil der Verkaufsprognose zu verfeinern, der die einzigartigen Herausforderungen der Weinwelt und die spezifischen Anforderungen ihres Produkts berücksichtigt.

<br>

### Projektstruktur

Das Ziel das Projekt ist eine explorative Datenanalyse (EDA) durchzuführen. Wir werden die ersten Einblick in der Daten erhalten, Muster identifizieren und Hypothesen aufstellen.
Die folgenden schritt werden in der Analyse durch durchgeführt

**1.  Datenvorbereitung**

        1.1 Datenimport: Laden der Verkaufsdaten aus CSV-Dateien oder einer Datenbank.

        1.2 Erste Datenanalyse: Überblick über Spalten, Datentypen und erste visuelle Inspektion.

        1.3 Datenbereinigung: Behandlung fehlender Werte, Entfernen von Dubletten und Identifikation von Ausreißern.

**2. Explorative Datenanalyse (EDA)**

        2.1  Deskriptive Statistik: Berechnung von Mittelwert, Median, Standardabweichung etc.
  
        2.2  Datenvisualisierung: Erstellen von Diagrammen zur Verteilung und Trends der Verkaufszahlen.
  
        2.3  Korrelationsanalyse: Untersuchung der Beziehungen zwischen verschiedenen Variablen.

**3. Feature Engineering**

         3.1 Erstellung von Dummy-Variablen: Umwandlung von kategorischen Variablen in numerische Werte (One-Hot-Encoding).
  
         3.2 Hinzufügen externer Regressoren: Berücksichtigung von Feiertagen, Produzenten, Ländern und Regionen als erklärende Variablen.
  
         3.3 Erstellung zeitbasierter Features: Z. B. Wochentag, Monat, Quartal, Feiertage oder saisonale Effekte.

**4. Modellierung mit Facebook Prophet**
   
       4.1 Modellerstellung: Definition des Prophet-Modells mit saisonalen Komponenten und Regressoren.
   
       4.2 Hyperparameter-Tuning mit Optuna: Optimierung von changepoint_prior_scale und seasonality_prior_scale zur Verbesserung der Vorhersagegenauigkeit. 
  
       4.3 Train-Test-Split: Aufteilung der Daten für Modelltraining und Evaluierung.
  

**5. Modellbewertung**
   
       5.1 Cross-Validation (Zeitreihen-Validierung): Evaluierung des Modells mit zeitbasierten Splits.
   
       5.2 Fehlermetriken berechnen: MAPE, MAE und RMSE zur Beurteilung der Modellleistung.
  
       5.3 Ergebnisse visualisieren: Vergleich der Vorhersagen mit den tatsächlichen Verkaufswerten.

**6. Erkenntnisse & Optimierung**
   
       6.1 Analyse der Ergebnisse: Identifikation von Verbesserungspotenzialen.
    
       6.2 Modellanpassungen: Feinabstimmung der Hyperparameter und Feature-Engineering zur Optimierung.
 
       6.3 Dokumentation & Fazit: Zusammenfassung der wichtigsten Erkenntnisse und zukünftige Optimierungsmöglichkeiten.


<br>



### Analysis 

Basierend auf den Prognoseergebnissen und der Modellbewertung lassen sich gezielte Maßnahmen zur Optimierung der Bestandsverwaltung und Verkaufsstrategie ableiten. Die Analyse beantwortet zentrale.


**1. Welche Produkte sind die Bestseller, und welchen Beitrag leisten sie zum Geschäftserfolg?**
   
       + Identifikation der umsatzstärksten Produkte zur gezielten Sortimentssteuerung.
       + Fokus auf die Optimierung der Bestände dieser Artikel, um Nachfragespitzen abzudecken.
  
**2. Wie kann die Bestandsverwaltung verbessert werden?**
   
       + Anpassung der Bestellmengen basierend auf den Verkaufsprognosen, um Überbestände und Engpässe zu vermeiden.
       + Implementierung datengetriebener Lagerstrategien für eine effizientere Kapitalbindung.

**3. Wie rentabel sind einzelne Bestellungen?**
   
       + Analyse der Rentabilität pro Bestellung unter Berücksichtigung von durchschnittlichen Versandkosten und Warenkorbwerten.
       + Optimierung von Rabatt- und Lieferstrategien zur Steigerung der Gewinnmargen.
     
**4. Welchen Einfluss haben verschiedene Monate und Jahreszeiten auf den Umsatz?**
   
       + Identifikation saisonaler Nachfragemuster zur besseren Planung von Marketing- und Verkaufsstrategien.
       + Erhöhung des Lagerbestands in Hochsaison-Phasen, um Nachfragespitzen abzudecken.
     
**5. Welche Artikel haben eine längere Verkaufsdauer?**
    
       + Ermittlung von Produkten mit niedriger Umschlagshäufigkeit, um gezielte Verkaufsförderungen oder Sortimentsanpassungen vorzunehmen.
       + Reduzierung von Ladenhütern durch gezielte Preisstrategien oder Marketingmaßnahmen.
      
**6. Wie entwickelt sich die aktuelle Nachfrage im Vergleich zu früheren Perioden?**
    
        + Vergleich der aktuellen Verkaufszahlen mit historischen Daten zur Identifikation von Wachstumstrends oder Rückgängen.
        + Nutzung dieser Erkenntnisse zur langfristigen Strategieplanung und Angebotsoptimierung.
        
<br>
Diese datenbasierten Erkenntnisse ermöglichen eine präzisere Steuerung des Geschäfts, minimieren Risiken und maximieren die Rentabilität durch eine optimierte Bestandsplanung.
 

<br>
<br>

Background in Python, Machine Learning and Mathematical Optimisation.
<br>
<br>



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
