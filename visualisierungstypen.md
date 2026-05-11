# Visualisierungstypen

Übersicht aller Diagramm- und Kartentypen, die für Datenvisualisierungen der Stadt Winterthur infrage kommen. Grundlage sind Abschnitt 6 der [Visualisierungsleitlinien](./stadt-winterthur-visualisierungsleitlinien.md); zusätzlich aufgenommen sind die Bevölkerungspyramide (Spezialfall des Tornadodiagramms, häufig in der amtlichen Statistik) sowie Karten mit lokalen WMS-Hintergrundebenen.

Spalte **Status**: ✓ = Beispiel im Repo vorhanden, — = noch offen.

## Diagramme

| Typ | Beschreibung | Status |
|-----|--------------|--------|
| Balkendiagramm | Horizontale Rechtecke; Vergleich kategorischer Werte. Varianten: einfach, gestapelt, gruppiert, divergierend. | — |
| Säulendiagramm | Vertikale Rechtecke; Vergleich kategorischer Werte. Varianten wie Balkendiagramm. | ✓ `echarts-dropdown.html`, `sszvis.html` |
| Liniendiagramm | Punkte durch Linien verbunden; zeitliche Veränderungen oder Verteilungen. Eine oder mehrere Linien. | — |
| Flächendiagramm | Wie Liniendiagramm, Fläche unter der Linie gefüllt. Varianten: einfach, gestapelt. | — |
| Kuchendiagramm / Donutdiagramm | Kreissektoren proportional zum Anteil; max. 6 Sektoren. | — |
| Streudiagramm (Scatterplot) | Beziehung zweier quantitativer Variablen; optional dritte Variable über Farbe. | — |
| Baumdiagramm (Treemap) | Verschachtelte Rechtecke für hierarchische Teil-Ganzes-Beziehungen. | — |
| Boxplot | Median, Quartile, Spannweite und Ausreisser; Verteilungsvergleich. | — |
| Rasterdiagramm (Waffeldiagramm) | 10×10-Gitter, jede Zelle 1 %; Fortschritts- oder Anteilsanzeige. | — |
| Heatmap | 2D-Matrix mit farbkodierten Zellen; nur divergierende Palette. | — |
| Radardiagramm (Spinnendiagramm) | Mehrere quantitative Variablen auf radialen Achsen. | — |
| Tornadodiagramm (Butterfly) | Zwei gegenüberliegende Kategorien auf gemeinsamer Skala; nur divergierende Palette. | — |
| Lollipop-Diagramm | Punkte am Ende von Linien; Alternative zum Balkendiagramm bei vielen oder hohen Werten. | — |
| **Bevölkerungspyramide** | Spezialfall des Tornadodiagramms: Altersgruppen auf der Y-Achse, Männer/Frauen als gegenüberliegende horizontale Balken. Klassiker der amtlichen Demografiestatistik. Vorbild: [sszvis population pyramid](https://statistikstadtzuerich.github.io/sszvis/#/population-pyramid). | ✓ `echarts-population-pyramid.html` (gestapelt nach Heimat Schweiz/Ausland) |

## Karten

| Typ | Beschreibung | Status |
|-----|--------------|--------|
| Choroplethen-Karte | Polygone (z. B. Quartiere) eingefärbt nach einem Wert; sequentielle Palette. | ✓ `echarts-choropleth.html` |
| Divergierende Choroplethen-Karte | Wie Choropleth, aber mit Mittelpunkt (z. B. Veränderung gegenüber Vorjahr); divergierende Palette. | — |
| Symbolkarte mit Punkten | Punkte zeigen Vorhandensein oder Häufung eines Merkmals (one-to-one / one-to-many). | — |
| Symbolkarte mit Kreisen | Kreisgrösse proportional zum Wert; geeignet für absolute Mengen pro Standort. | ✓ `leaflet.html`, `maplibre.html` (jeweils auf swisstopo-Basemap) |
| **Karte mit Winterthurer WMS-Hintergrundebene** | Datenebene überlagert auf städtischen Geodaten via WMS-Dienst des Stadt Winterthur Geo-Portals. Mögliche Hintergründe: amtlicher Stadtplan, Orthofoto, Amtliche Vermessung (Liegenschaften), Zonenplan, Baumkataster, Solarkataster, Klimaanalyse u. a. Quelle: [2D-Stadtplan Datenbeschreibung](https://stadt.winterthur.ch/themen/leben-in-winterthur/planen-und-bauen/wir-beraten-sie/geoinformation-und-vermessung/2d-stadtplan/2d-stadtplan-datenbeschreibung). | — |

## Zuordnung zu typischen Anwendungsfällen

| Anwendungszweck | Empfohlene Typen |
|-----------------|------------------|
| Kategorienvergleich | Balken-, Säulen-, Lollipop-Diagramm |
| Zeitlicher Verlauf | Linien-, Flächendiagramm |
| Teil-Ganzes-Beziehung | Kuchen-, Donut-, Baum-, Rasterdiagramm |
| Verteilung | Boxplot, Streudiagramm |
| Korrelation | Streudiagramm, Heatmap |
| Geografische Verteilung (Flächen) | Choroplethen-Karte |
| Geografische Verteilung (Standorte) | Symbolkarte mit Punkten oder Kreisen |
| Räumlicher Bezug zu städt. Infrastruktur | Karte mit WMS-Hintergrundebene |
| Bevölkerungsstruktur nach Alter und Geschlecht | Bevölkerungspyramide |
| Multivariate Vergleiche | Radardiagramm |
| Positiv/Negativ | Divergierendes Balken-/Säulendiagramm, divergierende Choropleth, Tornadodiagramm |
