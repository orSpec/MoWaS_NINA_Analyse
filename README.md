
## MoWaS_NINA_Analyse

**Github rendert Folium-Karten nicht - deshalb hier ein [Link zu nbviewer](https://nbviewer.jupyter.org/github/orSpec/MoWaS_NINA_Analyse/blob/master/Analyse_Meldungen.ipynb), wo das gesamte Notebook angezeigt wird.**


Motiviert durch den [bundesweiten Warntag 2020](https://warnung-der-bevoelkerung.de/) kam die Idee auf, zu analysieren, welche Meldungen durch [MoWaS](https://www.bbk.bund.de/DE/AufgabenundAusstattung/Krisenmanagement/WarnungderBevoelkerung/MoWaS/ModularesWarnsystem_node.html) (Modulares Warnsystem) an die Warn-App [NINA](https://www.bbk.bund.de/DE/NINA/Warn-App_NINA_node.html) gesendet wurden.

### Daten
Die zugrundeliegende PDF-Datei basiert auf einer [Anfrage](https://fragdenstaat.de/anfrage/ubersicht-uber-warnmeldungen-des-bevolkerungsschutzes-mithilfe-der-app-nina/) an das Bundesamt für Bevölkerungsschutz und Katastrophenhilfe. Die Datei enthält Warnmeldungen zwischen 2014 und 2017, die Daten sind also nicht wirklich aktuell. Pro Meldung ist die auslösende Stelle, der Anlass und die Anzahl der Aktualisierungen der Meldung angegeben. Es existiert zwar eine Spalte Handlungsempfehlung, allerdings ist diese nicht befüllt.

### Code
Die Analyse wurde in einem [Jupyter Notebook](https://jupyter.org/) mithilfe der folgenden Bibliotheken durchgeführt:

 - pandas
 - [camelot](https://camelot-py.readthedocs.io/en/master/) zum Einlesen der PDF-Datei
 - [matplotlib.pyplot](https://matplotlib.org/api/pyplot_api.html) und [seaborn](https://seaborn.pydata.org/) zur Visualisierung
 - [geopy](https://geopy.readthedocs.io/en/stable/#) zur Geokodierung
 - [folium](https://python-visualization.github.io/folium/) zum Erstellen von Karten
 - [scikit-learn](https://scikit-learn.org/) zum Finden der häufigsten Alarmanlässe i. V. m. deutschen Stoppwörtern vom  [NLTK - Natural Language Toolkit](https://www.nltk.org/)

