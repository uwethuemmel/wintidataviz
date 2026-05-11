# Bibliothekswahl: Charting & Mapping

Empfehlung für den Visualisierungs-Stack auf Basis der in [`visualisierungstypen.md`](./visualisierungstypen.md) aufgeführten Diagramm- und Kartentypen. Kriterien: Einfachheit, breite Nutzerbasis, Open Source, möglichst wenige Bibliotheken.

## Empfehlung

**ECharts (Apache 2.0) + Leaflet (BSD-2-Clause).**

Zwei Bibliotheken decken alle 15 Visualisierungstypen ab. Beide haben grosse, gepflegte Communities, beide sind genuin Open Source (OSI-konform), beide sind über CDN als einzelner Script-Tag nutzbar.

## Abdeckungsmatrix

| Visualisierungstyp | ECharts | Leaflet | Bemerkung |
|---|---|---|---|
| Säulen-/Balken-/gestapelt/gruppiert/divergierend | ✓ | — | Native, vollständig deklarativ |
| Linien-/Flächendiagramm (auch gestapelt) | ✓ | — | Native |
| Kuchen-/Donut | ✓ | — | Native |
| Streudiagramm | ✓ | — | Native; Farb- und Grössenkodierung möglich |
| Treemap | ✓ | — | Eigene Serie |
| Boxplot | ✓ | — | Native; `dataset`-Transform bildet Quartile |
| Rasterdiagramm (Waffle) | ✓ | — | Via `pictorialBar` oder Custom Series |
| Heatmap | ✓ | — | Native kartesische Heatmap-Serie |
| Radar | ✓ | — | Native |
| Tornadodiagramm | ✓ | — | Gespiegelte Bar-Serie mit negativen Werten |
| Bevölkerungspyramide | ✓ | — | Tornado-Muster; [ECharts-Beispiel](https://echarts.apache.org/examples/en/editor.html?c=bar-negative) |
| Lollipop | ✓ | — | `effectScatter` + Linie, oder Custom |
| Choroplethen-Karte | ✓ | ✓ | ECharts: `map`-Serie ohne Basemap. Leaflet: `L.geoJSON` über Tiles. |
| Symbolkarte (Kreise/Punkte) | △ | ✓ | ECharts kann geo-scatter, mit Basemap ist Leaflet natürlicher |
| Karte mit WMS-Hintergrund | — | ✓ | `L.tileLayer.wms()` ist erstklassig in Leaflet |

ECharts hat nur eine Lücke: WMS-Basemaps. Leaflet schliesst sie.

## Warum ECharts

- **Abdeckung**: Jeder Diagrammtyp aus den Leitlinien ist eine native Serie, ohne Plugins. Boxplot, Heatmap, Treemap, Radar und Tornado sind eingebaut — die meisten Konkurrenten brauchen für mindestens einen davon eine Erweiterung.
- **Open Source**: Apache 2.0, betrieben von der Apache Software Foundation. ~62k GitHub-Sterne, aktive Commits, eingesetzt bei Baidu, Alibaba, GitLab und vielen Dashboards im öffentlichen und privaten Sektor.
- **API**: Einziger deklarativer `setOption({...})`-Aufruf; gleiches mentales Modell über alle Diagrammtypen hinweg.
- **Anpassbarkeit**: Jedes visuelle Element ist überschreibbar — Paletten, Typografie, Achsenbeschriftungen. Kein "Library-Look", gegen den man kämpfen müsste.
- **Bundle**: ~1 MB minified im Full-Build; ~400 KB nach Tree-Shaking auf die benötigten Serien. CDN-tauglich.

## Warum Leaflet

- **WMS ist eingebaut**: `L.tileLayer.wms("https://.../wms", { layers, format, transparent })`. Sowohl das Winterthurer Geoportal (Stadtplan, Orthofoto, Zonenplan, Baumkataster, Solarkataster …) als auch swisstopo liefern Standard-WMS-Endpunkte — Leaflet konsumiert sie ohne Adapter.
- **Choropleth- und Symbolkarten-Idiome** sind kanonisch: `L.geoJSON(features, { style })` und `L.circleMarker` mit wenigen Optionen.
- **Open Source**: BSD-2-Clause; ~40k Sterne; seit 2011 ohne Unterbruch gepflegt. De-facto-Standard für Web-Karten ausserhalb der WebGL-Vector-Tile-Welt.
- **Ökosystem**: Hunderte Plugins (Clustering, Heatmaps, Zeichnen, Geocoding) für späteren Bedarf.
- **Bundle**: ~42 KB gzipped — federleicht.

## Verworfene Alternativen

| Bibliothek | Verworfen weil … |
|---|---|
| **Highcharts** | Sehr poliert, volle Abdeckung, aber CC-BY-NC-Quellverfügbarkeit — *kein* Open Source nach OSI. Kommerzielle Lizenz nötig für städtische Nutzung. |
| **Chart.js** | Grosse Community (~65k Sterne), aber Lücken: kein nativer Boxplot, Treemap, Radar (nur Basic), Tornado, Pyramide. 3–4 Plugins nötig — der Vorteil "weniger Bibliotheken" verkehrt sich in "mehr Plugins". |
| **Plotly.js** | MIT, ~17k Sterne, breite Abdeckung. Aber schwerer (~3 MB), starker "Plotly-Look", verbosere API als ECharts. Vertretbare Alternative, wenn statistische Diagramme (Violinplot, KDE) Priorität haben. |
| **D3 / Observable Plot / sszvis** | Maximale Kontrolle, kleinere Community, mehr Code pro Diagramm. sszvis ist auf das Stadt-Zürich-Designsystem zugeschnitten, nicht auf Winterthur. Nur einsetzen, wenn ECharts einen Typ nicht abdeckt oder druckfertige, hand-getunte Ausgabe nötig ist. |
| **MapLibre GL JS** | Besser für Vector Tiles und sehr grosse Datenmengen, aber WMS-Unterstützung nur als Workaround (Raster-Source). Nur als dritte Bibliothek, wenn explizit Vector-Tile-Ästhetik gefragt ist. |
| **OpenLayers** | GIS-nativ (Projektionen, WMTS, WFS, Druckexport), BSD-2, ~11k Sterne. Steilere Lernkurve als Leaflet. Empfehlung nur, falls Winterthurs WMS-Arbeit in Richtung echtes GIS wächst. |

## Ergänzende Tools für andere Output-Formen

Diese Werkzeuge konkurrieren nicht mit ECharts/Leaflet, sondern lösen eine **andere Aufgabe**: nicht «ein Chart ins CMS einbetten», sondern «ein Dokument mit Text und mehreren Charts publizieren». Daher kein Eintrag in der Abdeckungsmatrix oben, sondern eine eigene Empfehlungslinie.

### Quarto (MIT, Posit)

[Quarto](https://quarto.org) ist ein Open-Source-Publishing-System, das Markdown-Inhalte mit Code-Blöcken (R, Python, Julia, Observable JS) zu HTML, PDF, Word oder Reveal.js rendert. Die eigentlichen Diagramme entstehen darin durch eine *andere* Bibliothek — Observable Plot, Plotly, ECharts via Raw-HTML-Block, Leaflet via htmlwidgets. Quarto ersetzt unsere Bibliothekswahl also nicht, es **umschliesst** sie.

**Stark bei:**

| Szenario | Begründung |
|---|---|
| Datenstories (Fliesstext + 5–10 Visualisierungen + Quellen + Footnoten) | Markdown-first, exzellente Typografie, Cross-Refs eingebaut |
| Jahres-/Quartalsberichte, die parallel als Print-PDF und Web-HTML erscheinen sollen | Einziges Tool im Vergleich, das beide Formate aus einer Quelle erzeugt |
| Dashboards mit fixem Grid-Layout (Sidebars, Cards, Tabs) | Quarto Dashboards (≥1.4) liefern fertiges Layout-System |
| Reproduzierbarkeit: Datenstand zu einem Stichtag im Dokument einfrieren, archivieren | `quarto render` friert den Stand ein; gut versionierbar mit git |

**Nicht ideal bei:**

- **Einem Live-Chart pro CMS-Seite**: Quarto braucht einen Build-Schritt. Für Live-Daten via OJS-Blöcke schrumpft der Markdown-Vorteil, weil dann doch JS-Code direkt im Dokument lebt. Geplante Re-Renders via CI/CD passen nicht zu Update-Frequenzen «täglich oder häufiger».
- **Vollständige Typen-Abdeckung mit Quarto-Bordmitteln**: Choropleth + Bevölkerungspyramide + WMS + Heatmap erfordert Mischen mehrerer Bibliotheken *unter* Quarto (Plotly + Leaflet + OJS + Raw-ECharts). Dann sind es drei Bibliotheken plus Quarto statt zwei nackt.

**Empfehlung:** Quarto **danebenstellen**, nicht ersetzen. Für die «Daten und Statistik»-CMS-Seiten bleibt der ECharts+Leaflet-Stack der direkte Weg. Sobald narrative Formate, Print-Begleitausgaben oder mehrteilige Themen-Stories anstehen, wird Quarto sinnvoll — die HTML-Diagramme darin können weiter mit ECharts oder Observable Plot gerendert werden.

## Fazit

**Stack: ECharts für alles Diagrammhafte plus Choropleth ohne Basemap; Leaflet für alles mit Basemap (insbesondere WMS).** Zwei Scripts, zwei CDN-URLs, zwei API-Oberflächen zu lernen, volle Abdeckung von `visualisierungstypen.md`, beide Open Source, beide 40k+ Sterne Community, beide seit über einem Jahrzehnt gepflegt.

Optionale Erweiterung bei Bedarf:

- **OpenLayers**, falls die WMS-Arbeit in Richtung vollwertiges GIS wächst (mehrere Projektionen, Druckexport, komplexe Layer-Verwaltung).
- **Quarto** als parallele Publikations-Schiene für Datenstories und Print-/Web-Berichte (siehe Abschnitt oben).
