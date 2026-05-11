# Visualisierungs-Beispiele

Minimalbeispiele für Datenvisualisierungen mit verschiedenen Open-Source-Bibliotheken am Beispiel offener Daten der Stadt Winterthur. Jedes Beispiel ist eine eigenständige HTML-Datei, die ihre Abhängigkeiten per CDN lädt — kein Build-Schritt, kein `npm install`.

Eine Übersicht aller Beispiele mit kurzer Bibliotheksbeschreibung gibt es in [`index.html`](./index.html).

## Beispiele

### Diagramme

- [`echarts-dropdown.html`](./echarts-dropdown.html) — Säulendiagramm mit Jahres-Dropdown (Apache ECharts)
- [`echarts-population-pyramid.html`](./echarts-population-pyramid.html) — Bevölkerungspyramide, Geschlecht × Heimat (Apache ECharts)
- [`sszvis.html`](./sszvis.html) — Säulendiagramm im sszvis-Design (Statistik Stadt Zürich)

### Karten

- [`leaflet.html`](./leaflet.html) — Symbolkarte mit Kreisen, Basemap CARTO Positron, Stadtumriss als Maske
- [`maplibre.html`](./maplibre.html) — Gleiche Daten als Vektorkarte auf swisstopo-Basis
- [`echarts-choropleth.html`](./echarts-choropleth.html) — Choropleth Einwohner pro Quartier, ohne Basemap (Apache ECharts)

### Quarto (Datenstory-Pattern)

- [`quarto-example.qmd`](./quarto-example.qmd) — Säulendiagramm der Bevölkerung Winterthur nach Altersklasse, mit **Live-Datenanbindung** und Jahres-Slider (Observable Plot, OJS-Blöcke in Quarto). Render mit `quarto render quarto-example.qmd`.
- [`quarto-example-python.qmd`](./quarto-example-python.qmd) — Gleiches Säulendiagramm im **Python-Workflow**: pandas zieht die CSV beim Build, Plotly rendert den interaktiven Chart. Datenstand zur Build-Zeit eingefroren — typisches Muster für Datenstories und Jahresberichte. Voraussetzung: `pip install pandas plotly jupyter` (idealerweise in einem venv).

## Lokal starten

Die Beispiele laden CSV und GeoJSON per `fetch` und funktionieren daher nicht über `file://`. Ein lokaler HTTP-Server genügt:

```sh
python3 -m http.server 8000
```

Anschliessend [http://localhost:8000/](http://localhost:8000/) öffnen.

## Datenquellen

Offene Daten der Stadt Winterthur, bereitgestellt über den Datenkatalog des Statistischen Amts Kanton Zürich:

- [Besuche Kultureinrichtungen](https://www.zh.ch/de/politik-staat/statistik-daten/datenkatalog.html#/datasets/2902@stadt-winterthur) — Säulendiagramme und Punktkarten
- [Einwohner pro Quartier](https://www.zh.ch/de/politik-staat/statistik-daten/datenkatalog.html#/datasets/2702@stadt-winterthur) — Choropleth
- [Bevölkerung nach Alter, Geschlecht und Heimat](https://www.zh.ch/de/politik-staat/statistik-daten/datenkatalog.html#/datasets/2605@stadt-winterthur) — Bevölkerungspyramide
- [`winterthur_quartiere_simplified.geojson`](./winterthur_quartiere_simplified.geojson) — lokale Datei, vereinfachte Quartiergrenzen Winterthur (WGS 84)

## Weiterführende Dokumente

- [`visualisierungstypen.md`](./visualisierungstypen.md) — Übersicht aller Diagramm- und Kartentypen mit Status (im Repo umgesetzt / offen)
- [`bibliothekswahl.md`](./bibliothekswahl.md) — Begründung der Bibliothekswahl (ECharts + Leaflet als minimaler Stack)
- [`stadt-winterthur-visualisierungsleitlinien.md`](./stadt-winterthur-visualisierungsleitlinien.md) — Farbpaletten, Diagrammtypen-Regeln, Departement-Farben der Stadt Winterthur
