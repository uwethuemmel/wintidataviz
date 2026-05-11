# Visualisierungsleitlinien der Stadt Winterthur – Farbpaletten & Diagrammtypen

Dieses Dokument enthält die verbindlichen Regeln für Datenvisualisierungen der Stadt Winterthur. Es umfasst Farbpaletten (Corporate, kategorisch, sequentiell, divergierend) sowie alle zulässigen Diagrammtypen mit ihren Varianten und Farbzuweisungen. Alle Farben sind barrierefrei gemäss WCAG 2.2.

Nutze dieses Dokument als vollständige Referenz, wenn du Datenvisualisierungen für die Stadt Winterthur erstellst oder prüfst.

---

## Allgemeine Grundsätze

- Die Höhe einer Visualisierung ist variabel; die Breite richtet sich nach dem Publikationsmedium (digital oder Print).
- Es sind ausschliesslich die hier definierten Farbpaletten zu verwenden. Das Farbschema schafft eine klare Wiedererkennbarkeit über alle Plattformen hinweg.
- Farben dienen dazu, Elemente zu unterscheiden oder zu verbinden, und sollen die Botschaft und Lesbarkeit unterstützen.
- Die Legende soll logisch und leicht lesbar sein.
- Farben sind als HEX-Codes angegeben. Für den Druck (CMYK) immer ein "Gut zum Druck" erstellen.

---

## 1. Corporate Farben

Verwendung für grundlegende Layout-Elemente wie Titel- und Textfarben. Quelle: Style-Guide der Stadt Winterthur.

| Name      | HEX     |
|-----------|---------|
| Weiss     | #FFFFFF |
| Hellgrau  | #ECECEA |
| Grau      | #DADAD6 |
| Anthrazit | #44443F |
| Schwarz   | #000000 |
| Rot       | #FF1900 |

---

## 2. Kategorische (qualitative) Farbpalette

**Zweck:** Darstellung von Kategorien ohne inhärente Reihenfolge oder Beziehung (z. B. Typen, Beschriftungen, Regionen, Departemente).

**Regeln:**
- Farben immer in der festgelegten Reihenfolge (01–06) verwenden.
- Farben 08–09 sind Erweiterungen für Anwendungen mit mehr als 6 Kategorien (z. B. 8 Departemente der Stadt Winterthur). Sie wurden in gleicher Sättigung und Logik wie 01–06 abgeleitet und füllen die grössten Lücken im Farbkreis (Orange bei H=35°, Pink bei H=330°).
- Farbe 07 (Grau) ist reserviert für neutrale Klassen wie "Total", "Andere" oder "Unbekannt" und zählt nicht als Kategoriefarbe.

| Nr. | Name            | HEX     | HSL-Referenz          |
|-----|-----------------|---------|-----------------------|
| 01  | Rot (500)       | #CB2512 | H=6° S=84% L=43%     |
| 02  | Violett (400)   | #A554C7 | H=282° S=51% L=55%   |
| 03  | Blau (300)      | #1592C0 | H=196° S=80% L=42%   |
| 04  | Petrol (500)    | #0C6974 | H=186° S=81% L=25%   |
| 05  | Grün (300)      | #1E9B6F | H=159° S=68% L=36%   |
| 06  | Rot (100)       | #F1A79F | H=6° S=75% L=78%     |
| 07  | Grau (300)      | #898989 | H=0° S=0% L=54%      |
| 08  | Orange (500)    | #C07915 | H=35° S=80% L=42%    |
| 09  | Pink (500)      | #BD377A | H=330° S=55% L=48%   |

---

## 3. Sequentielle Farbpaletten

**Zweck:** Darstellung von Daten, die sich von niedrigen zu hohen Werten entwickeln (z. B. Mengen, Prozentsätze, Rangfolgen).

**Regeln:**
- Helle Farben = niedrige Werte, dunkle Farben = hohe Werte.
- Maximal 7 Abstufungen (Stufe 100–700).
- Für Kartenvisualisierungen sind bis zu 10 Abstufungen erlaubt (050–900).

### 3.1 Rot

| Stufe | HEX     | Ist kategorische Farbe?   |
|-------|---------|---------------------------|
| 050   | #F5BFBA | – (nur Karten)            |
| 100   | #F1A79F | = 06 Rot (kategorisch)    |
| 200   | #EC8B80 |                           |
| 300   | #E66254 |                           |
| 400   | #E2402E |                           |
| 500   | #CB2512 | = 01 Rot (kategorisch)    |
| 600   | #AA1F0F |                           |
| 700   | #89190C |                           |
| 800   | #681309 | – (nur Karten)            |
| 900   | #500F07 | – (nur Karten)            |

### 3.2 Violett

| Stufe | HEX     | Ist kategorische Farbe?      |
|-------|---------|------------------------------|
| 050   | #E2C3EF | – (nur Karten)               |
| 100   | #D3A3E6 |                              |
| 200   | #C88BE0 |                              |
| 300   | #BC6CDD |                              |
| 400   | #A554C7 | = 02 Violett (kategorisch)   |
| 500   | #86499F |                              |
| 600   | #6F3E85 |                              |
| 700   | #583168 |                              |
| 800   | #432650 | – (nur Karten)               |
| 900   | #341E3D | – (nur Karten)               |

### 3.3 Blau

| Stufe | HEX     | Ist kategorische Farbe?   |
|-------|---------|---------------------------|
| 050   | #99D7EE | – (nur Karten)            |
| 100   | #71C2E0 |                           |
| 200   | #47ACD1 |                           |
| 300   | #1590BE | = 03 Blau (kategorisch)   |
| 400   | #1178A9 |                           |
| 500   | #0E679D |                           |
| 600   | #095A8A |                           |
| 700   | #094372 |                           |
| 800   | #063062 | – (nur Karten)            |
| 900   | #03225E | – (nur Karten)            |

### 3.4 Petrol

| Stufe | HEX     | Ist kategorische Farbe?    |
|-------|---------|----------------------------|
| 050   | #B0CFD0 | – (nur Karten)             |
| 100   | #97BFC1 |                            |
| 200   | #78A9AC |                            |
| 300   | #3F9399 |                            |
| 400   | #267F87 |                            |
| 500   | #0C6974 | = 04 Petrol (kategorisch)  |
| 600   | #075765 |                            |
| 700   | #064756 |                            |
| 800   | #073542 | – (nur Karten)             |
| 900   | #072833 | – (nur Karten)             |

### 3.5 Grün

| Stufe | HEX     | Ist kategorische Farbe?  |
|-------|---------|--------------------------|
| 050   | #96D6BD | – (nur Karten)           |
| 100   | #71C89C |                          |
| 200   | #3DB578 |                          |
| 300   | #1EA160 | = 05 Grün (kategorisch)  |
| 400   | #1E8353 |                          |
| 500   | #1C6C46 |                          |
| 600   | #1C5C3E |                          |
| 700   | #194933 |                          |
| 800   | #153628 | – (nur Karten)           |
| 900   | #112B1F | – (nur Karten)           |

### 3.6 Grau

| Stufe | HEX     | Ist kategorische Farbe?  |
|-------|---------|--------------------------|
| 050   | #CCCCCC | – (nur Karten)           |
| 100   | #B6B6B6 |                          |
| 200   | #A0A0A0 |                          |
| 300   | #898989 | = 07 Grau (kategorisch)  |
| 400   | #707070 |                          |
| 500   | #61615E |                          |
| 600   | #52524F |                          |
| 700   | #44443F |                          |
| 800   | #31312E | – (nur Karten)           |
| 900   | #242422 | – (nur Karten)           |

### 3.7 Orange

Abgeleitet von der kategorischen Farbe 08 (Orange, H=35°) in gleicher Sättigungs- und Helligkeitslogik wie die bestehenden Skalen.

| Stufe | HEX     | Ist kategorische Farbe?    |
|-------|---------|----------------------------|
| 100   | #EDC081 |                            |
| 200   | #E8AA53 |                            |
| 300   | #E59523 |                            |
| 400   | #D98816 |                            |
| 500   | #C47A11 | ≈ 08 Orange (kategorisch)  |
| 600   | #A0630C |                            |
| 700   | #7C4C08 |                            |

### 3.8 Pink

Abgeleitet von der kategorischen Farbe 09 (Pink, H=330°) in gleicher Sättigungs- und Helligkeitslogik wie die bestehenden Skalen.

| Stufe | HEX     | Ist kategorische Farbe?  |
|-------|---------|--------------------------|
| 100   | #DB93B7 |                          |
| 200   | #D273A3 |                          |
| 300   | #CB528E |                          |
| 400   | #C94084 |                          |
| 500   | #C1337A | ≈ 09 Pink (kategorisch)  |
| 600   | #A32866 |                          |
| 700   | #841F51 |                          |

### 3.9 Empfohlene Skalenauswahl (sequentiell)

Je nach Anzahl benötigter Stufen die folgenden Abstufungen verwenden (Beispiel Rot – gleiches Prinzip gilt für alle Farbreihen):

| Anzahl Stufen | Verwendete Stufen                      |
|---------------|----------------------------------------|
| 1             | 500                                    |
| 2             | 100, 500                               |
| 3             | 100, 300, 500                          |
| 4             | 100, 300, 500, 700                     |
| 5             | 100, 200, 300, 500, 700               |
| 6             | 100, 200, 300, 400, 500, 700          |
| 7             | 100, 200, 300, 400, 500, 600, 700     |

Für Karten (8–10 Stufen): zusätzlich 050 am Anfang und 800/900 am Ende anfügen.

---

## 4. Divergierende Farbpaletten

**Zweck:** Darstellung von Daten mit einem aussagekräftigen Mittelpunkt oder einer Abweichung von einer Norm (z. B. Unterschiede, Änderungen, Vergleiche).

**Aufbau:** Zwei kontrastierende Farben an den Enden, getrennt durch eine neutrale Farbe (Grau #CCCCCC oder #B6B6B6) oder direkt aneinander anschliessend.

### 4.1 Farbskala 01 – Standard (Rot ↔ Blau)

**Verwendung:** Standardmässige divergierende Palette, sofern kein spezifisches Thema vorliegt.

- Negativer Pol: Rot-Skala (dunkel → hell: #89190C → #CB2512 → #E66254 → #EC8B80 → #F1A79F)
- Neutraler Mittelpunkt (optional): #CCCCCC
- Positiver Pol: Blau-Skala (hell → dunkel: #71C2E0 → #47ACD1 → #1590BE → #1178A9 → #0E679D → #095A8A → #094372)

| Anzahl Farben | Werte |
|---------------|-------|
| 2 | #CB2512, #1590BE |
| 3 | #CB2512, #B6B6B6, #1590BE |
| 5 (mit Mitte) | #CB2512, #F1A79F, #CCCCCC, #71C2E0, #1590BE |
| 7 (ohne Mitte) | #CB2512, #E66254, #F1A79F, #71C2E0, #1590BE, #0E679D, (+ ggf. #89190C / #094372) |
| 9 (mit Mitte) | #89190C, #CB2512, #E66254, #F1A79F, #CCCCCC, #71C2E0, #1590BE, #0E679D, #094372 |
| Max. 15 | #89190C, #AA1F0F, #CB2512, #E2402E, #E66254, #EC8B80, #F1A79F, #CCCCCC, #71C2E0, #47ACD1, #1590BE, #1178A9, #0E679D, #095A8A, #094372 |

### 4.2 Farbskala 02 – Geschlecht (Violett ↔ Grün)

**Verwendung:** Darstellungen mit Bezug auf Geschlecht oder ähnliche binäre Kategorien.

- Pol A: Violett-Skala (dunkel → hell: #583168 → #6F3E85 → #86499F → #A554C7 → #BC6CDD → #C88BE0 → #D3A3E6)
- Neutraler Mittelpunkt (optional): #CCCCCC
- Pol B: Grün-Skala (hell → dunkel: #71C89C → #3DB578 → #1EA160 → #1E8353 → #1C6C46 → #1C5C3E → #194933)

| Anzahl Farben | Werte |
|---------------|-------|
| 2 | #A554C7, #1EA160 |
| 3 | #A554C7, #B6B6B6, #1EA160 |
| 5 (mit Mitte) | #A554C7, #D3A3E6, #CCCCCC, #71C89C, #1EA160 |
| 8 (ohne Mitte) | #583168, #86499F, #BC6CDD, #D3A3E6, #71C89C, #1EA160, #1C6C46, #194933 |
| Max. 15 | #583168, #6F3E85, #86499F, #A554C7, #BC6CDD, #C88BE0, #D3A3E6, #CCCCCC, #71C89C, #3DB578, #1EA160, #1E8353, #1C6C46, #1C5C3E, #194933 |

### 4.3 Farbskala 03 – Positiv/Negativ (Rot ↔ Petrol)

**Verwendung:** Darstellungen mit "Positiv/Negativ"- oder "Ja/Nein"-Werten.

- Negativer Pol: Rot-Skala (dunkel → hell: #89190C → #AA1F0F → #CB2512 → #E2402E → #E66254 → #EC8B80 → #F1A79F)
- Neutraler Mittelpunkt (optional): #CCCCCC
- Positiver Pol: Petrol-Skala (hell → dunkel: #97BFC1 → #78A9AC → #3F9399 → #267F87 → #0C6974 → #075765 → #064756)

| Anzahl Farben | Werte |
|---------------|-------|
| 2 | #CB2512, #0C6974 |
| 3 | #CB2512, #B6B6B6, #0C6974 |
| 5 (mit Mitte) | #CB2512, #F1A79F, #CCCCCC, #97BFC1, #0C6974 |
| 8 (ohne Mitte) | #89190C, #CB2512, #E66254, #F1A79F, #97BFC1, #3F9399, #0C6974, #064756 |
| Max. 15 | #89190C, #AA1F0F, #CB2512, #E2402E, #E66254, #EC8B80, #F1A79F, #CCCCCC, #97BFC1, #78A9AC, #3F9399, #267F87, #0C6974, #075765, #064756 |

---

## 5. Entscheidungshilfe: Welche Farbpalette verwenden?

| Datentyp | Palette | Beispiel |
|----------|---------|----------|
| Diskrete Kategorien ohne Rangfolge | Kategorisch (Abschnitt 2) | Regionen, Typen, Beschriftungen |
| Geordnete Werte (niedrig → hoch) | Sequentiell (Abschnitt 3) | Mengen, Prozentsätze, Rangfolgen |
| Karten mit vielen Abstufungen | Sequentiell erweitert (050–900) | Choroplethenkarten |
| Abweichung von einer Norm | Divergierend Skala 01 (Abschnitt 4.1) | Differenzen, Veränderungen |
| Geschlechterbezogene Daten | Divergierend Skala 02 (Abschnitt 4.2) | Männlich/Weiblich |
| Positiv/Negativ-Bewertungen | Divergierend Skala 03 (Abschnitt 4.3) | Ja/Nein, Zunahme/Abnahme |
| Neutrale Sammelkategorie | Kategorisch Farbe 07 (#898989) | "Total", "Andere", "Unbekannt" |

### Zusätzliche Hinweise zu Skalentypen

- **Ordinal:** Daten mit Rangordnung, aber ungleichen Abständen (z. B. Gold, Silber, Bronze). → Sequentielle oder divergierende Palette verwenden.
- **Intervall:** Feste Messeinheit, aber kein absoluter Nullpunkt (z. B. Celsius-Temperatur). → Sequentielle oder divergierende Palette verwenden.
- **Verhältnis:** Feste Messeinheit mit absolutem Nullpunkt (z. B. Länge in Metern). → Sequentielle oder divergierende Palette verwenden.

---

## 6. Diagrammtypen – Übersicht und Regeln

Dieser Abschnitt beschreibt alle zulässigen Diagrammtypen, ihre Varianten, Einsatzzwecke und die jeweils zu verwendenden Farbpaletten.

### 6.1 Balkendiagramm

**Beschreibung:** Visualisiert kategorische Daten mit horizontalen Rechtecken. Die Y-Achse zeigt die Kategorien, die X-Achse die Werte. Die Länge der Balken ist proportional zu den dargestellten Werten.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Einfaches Balkendiagramm | Einfache, übersichtliche Ansicht zum Vergleich von Werten über eine Metrik. |
| Gestapeltes Balkendiagramm | Jeder Balken wird durch Farbe in Dimensionselemente aufgeteilt; die Gesamthöhe bleibt erhalten. Zeigt eine zusätzliche Dimension. |
| Gruppiertes Balkendiagramm | Zwei oder mehr Datensätze werden nebeneinander angezeigt und unter Kategorien auf derselben Achse gruppiert. |
| Divergierendes Balkendiagramm | Für Daten mit positiven und negativen Werten. Die Nulllinie ist immer schwarz hervorgehoben. |

**Farbregeln:** Kategorische Daten ohne Reihenfolge → Kategorische Palette (Abschnitt 2). Daten mit natürlicher Reihenfolge → Sequentielle (Abschnitt 3) oder Divergierende Palette (Abschnitt 4).

---

### 6.2 Säulendiagramm

**Beschreibung:** Wie ein Balkendiagramm, aber mit vertikalen Rechtecken. Die X-Achse zeigt die Kategorien, die Y-Achse die Werte.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Einfaches Säulendiagramm | Vergleich von Werten über die Höhe einer Metrik. |
| Gestapeltes Säulendiagramm | Jeder Balken wird durch Farbe in Dimensionselemente aufgeteilt; zeigt eine zusätzliche Dimension. |
| Gruppiertes Säulendiagramm | Zwei oder mehr Datensätze nebeneinander, unter Kategorien auf derselben Achse gruppiert. |
| Divergierendes Säulendiagramm | Für Daten mit positiven und negativen Werten. Die Nulllinie ist immer schwarz hervorgehoben. |

**Farbregeln:** Kategorische Daten ohne Reihenfolge → Kategorische Palette (Abschnitt 2). Daten mit natürlicher Reihenfolge → Sequentielle (Abschnitt 3) oder Divergierende Palette (Abschnitt 4).

---

### 6.3 Liniendiagramm

**Beschreibung:** Punkte, die durch Linien verbunden sind. Zeigt Veränderungen von Werten über die Zeit oder Verteilungen. Geeignet für eine oder mehrere Variablen.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Einfaches Liniendiagramm | Zeigt die Veränderung einer Variable in gleichen Zeitabständen. |
| Mehrere Linien | Vergleich der Entwicklung mehrerer Variablen im Zeitverlauf. |

**Farbregeln:** Kategorische Daten ohne Reihenfolge → Kategorische Palette (Abschnitt 2). Daten mit natürlicher Reihenfolge → Sequentielle (Abschnitt 3) oder Divergierende Palette (Abschnitt 4).

---

### 6.4 Flächendiagramm

**Beschreibung:** Stellt die Entwicklung von Mengen dar. Die Flächen zwischen Achse und Linien werden farblich hervorgehoben.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Einfaches Flächendiagramm | Erfüllt die gleiche Funktion wie ein einfaches Liniendiagramm, mit farblich gefüllter Fläche. |
| Gestapeltes Flächendiagramm | Zeigt die Entwicklung mehrerer Gruppen übereinander. Ermöglicht die Darstellung der Gesamtsumme und des Anteils jeder Gruppe in einer Grafik. |

**Farbregeln:** Kategorische Daten ohne Reihenfolge → Kategorische Palette (Abschnitt 2). Daten mit natürlicher Reihenfolge → Sequentielle (Abschnitt 3) oder Divergierende Palette (Abschnitt 4).

---

### 6.5 Kuchendiagramm / Donutdiagramm

**Beschreibung:** Ein Kreis, unterteilt in Sektoren, die den Ausprägungen einer qualitativen Variable entsprechen. Zeigt den Anteil jedes Sektors im Verhältnis zur Gesamtzahl.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Kuchendiagramm | Kreissektoren mit Bogenlänge, Winkel und Fläche proportional zum dargestellten Wert. |
| Donutdiagramm | Wie Kuchendiagramm, aber mit leerem Zentrum. Kategorien um den zentralen Bereich angeordnet. |

**Wichtige Einschränkungen:**
- Maximal 6 Abschnitte verwenden. Zu viele dünne Abschnitte sind schwer lesbar.
- Eine Legende ist erforderlich. Platzierung: rechts neben dem Diagramm, bei Platzmangel unterhalb.

**Farbregeln:** Kategorische Daten ohne Reihenfolge → Kategorische Palette (Abschnitt 2). Daten mit natürlicher Reihenfolge → Sequentielle (Abschnitt 3) oder Divergierende Palette (Abschnitt 4).

---

### 6.6 Streudiagramm (Scatterplot)

**Beschreibung:** Punkte zeigen die Beziehung zwischen zwei quantitativen Variablen. X-Achse = erste Variable, Y-Achse = zweite Variable. Eine dritte qualitative Variable kann durch Farbe oder Form der Punkte dargestellt werden.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Einfaches Streudiagramm | Zwei Metriken, jeder Achse eine Metrik zugeordnet. |
| Kategorisches Streudiagramm | Farbe der Punkte entspricht einer Kategorie. Maximal 6 Kategorien. Legende erforderlich. |

**Farbregeln:** Kategorische Daten ohne Reihenfolge → Kategorische Palette (Abschnitt 2). Daten mit natürlicher Reihenfolge → Sequentielle (Abschnitt 3) oder Divergierende Palette (Abschnitt 4).

---

### 6.7 Karten

**Beschreibung:** Thematische Karten zur Darstellung geografischer Daten. Verschiedene Kartentypen je nach Datenart.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Choroplethen-Karte | Gebiete eingefärbt im Verhältnis zur Verteilungsdichte. Zeigt, wie eine Messgrösse in einem geografischen Gebiet variiert. |
| Divergierende Choroplethen-Karte | Für Daten mit positiven und negativen Werten auf der Karte. |
| Symbolkarte mit Punkten | Punkte zeigen das Vorhandensein eines Merkmals an. Bereiche mit vielen Punkten = hohe Konzentration. Jeder Punkt kann eine einzelne Aufzeichnung (one-to-one) oder eine bestimmte Menge (one-to-many) darstellen. |
| Symbolkarte mit Kreisen | Kreise visualisieren Lage und Proportionen. Kreisgrösse proportional zum Wert. |

**Farbregeln:** Kategorische Daten → Kategorische Palette (Abschnitt 2). Geordnete Werte → Sequentielle Palette erweitert mit 050–900 (Abschnitt 3). Divergierende Daten → Divergierende Palette (Abschnitt 4).

---

### 6.8 Baumdiagramm (Treemap)

**Beschreibung:** Hierarchische Daten als verschachtelte Rechtecke. Alternative zum Kreisdiagramm für Teil-Ganzes-Beziehungen mit vielen Kategorien. Geeignet, wenn exakte Vergleiche nicht das Hauptanliegen sind.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Baumdiagramm | Verschachtelte Rechtecke für hierarchische Teil-Ganzes-Beziehungen mit grosser Kategorienzahl. |

**Farbregeln:** Kategorische Daten ohne Reihenfolge → Kategorische Palette (Abschnitt 2). Daten mit natürlicher Reihenfolge → Sequentielle (Abschnitt 3) oder Divergierende Palette (Abschnitt 4).

---

### 6.9 Boxplot

**Beschreibung:** Zeigt alle wichtigen robusten Lage- und Streumasse sowie die Spannweite eines Datensatzes: Median, oberes/unteres Quartil, Maximum/Minimum. Ausreisser können als einzelne Punkte eingezeichnet werden. Ermöglicht den Vergleich der Verteilung über mehrere Kategorien.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Boxplot | Zeigt Median, Quartile, Extremwerte und Ausreisser. Die Abstände geben Streuung und Schiefe an. |

**Farbregeln:** Kategorische Daten ohne Reihenfolge → Kategorische Palette (Abschnitt 2). Daten mit natürlicher Reihenfolge → Sequentielle (Abschnitt 3) oder Divergierende Palette (Abschnitt 4).

---

### 6.10 Rasterdiagramm (Waffeldiagramm / Gridplot)

**Beschreibung:** Stellt Anteile im Verhältnis zum Ganzen dar. Besteht aus einem 10×10-Gitter, wobei jede Zelle 1 % entspricht. Geeignet für Fortschritt in Richtung eines Ziels oder Prozentsatz der Erfüllung.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Rasterdiagramm | 10×10 Zellen = 100 %. Farbige Zellen zeigen den Anteil. Kann eine oder mehrere Kategorien enthalten. |

**Farbregeln:** Kategorische Daten ohne Reihenfolge → Kategorische Palette (Abschnitt 2). Daten mit natürlicher Reihenfolge → Sequentielle (Abschnitt 3) oder Divergierende Palette (Abschnitt 4).

---

### 6.11 Heatmap

**Beschreibung:** Zweidimensionale Matrix zur Darstellung der Beziehung zwischen zwei Variablen. Jede Zelle enthält einen numerischen Wert mit farblicher Kodierung: intensivere/dunklere Farbe bei höheren Werten. Nützlich für die Erkennung von Korrelationsmustern.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Heatmap | Visualisierung der Varianz über mehrere Variablen hinweg zur Anzeige von Korrelationsmustern. |

**Farbregeln:** Ausschliesslich die Divergierende Farbpalette (Abschnitt 4) verwenden.

---

### 6.12 Radardiagramm (Spinnendiagramm)

**Beschreibung:** Vergleicht mehrere quantitative Variablen. Jede Variable wird durch eine radiale Achse vom Zentrum aus dargestellt. Alle Achsen sind gleichmässig angeordnet und haben denselben Massstab. Die Verbindung der Punkte bildet ein Polygon.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Einfaches Radardiagramm | Eine Gruppe von Werten über mehrere gemeinsame Variablen. |
| Radardiagramm mit mehreren Gruppen | Mehrere Gruppen überlagert. Legende erforderlich. |

**Farbregeln:** Kategorische Daten ohne Reihenfolge → Kategorische Palette (Abschnitt 2). Daten mit natürlicher Reihenfolge → Sequentielle (Abschnitt 3) oder Divergierende Palette (Abschnitt 4).

---

### 6.13 Tornadodiagramm (Butterfly Chart)

**Beschreibung:** Vergleicht zwei Variablen oder Kategorien auf derselben numerischen Skala nebeneinander. Ermöglicht schnelles Erkennen von Unterschieden. Die Alterspyramide ist ein klassisches Beispiel.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Gestapeltes Tornadodiagramm | Vergleich von zwei Kategorien. Nulllinie immer schwarz hervorgehoben. Optional: Stapeln von zwei Balken pro Seite für weitere Unterteilung. |
| Gruppiertes Tornadodiagramm | Zwei oder mehr Kategorien nebeneinander auf derselben Achse gruppiert. |

**Farbregeln:** Ausschliesslich die Divergierende Farbpalette (Abschnitt 4) verwenden.

---

### 6.14 Lollipop-Diagramm

**Beschreibung:** Alternative zum Balkendiagramm für die Darstellung vieler Werte – besonders wenn Werte in einem hohen Bereich liegen (z. B. 80–90 % von 100 %). Ein Balkendiagramm kann in diesem Fall visuell aggressiv wirken, da es viel farbige Fläche einnimmt.

**Varianten:**

| Variante | Beschreibung |
|----------|-------------|
| Einfaches Lollipop-Diagramm | Punkte am Ende von Linien statt gefüllter Balken. Visuell leichter als ein Balkendiagramm bei vielen oder hohen Werten. |

**Farbregeln:** Kategorische Daten ohne Reihenfolge → Kategorische Palette (Abschnitt 2). Daten mit natürlicher Reihenfolge → Sequentielle (Abschnitt 3) oder Divergierende Palette (Abschnitt 4).

---

## 7. Schnellreferenz: Diagrammtyp → Farbpalette

| Diagrammtyp | Farbpalette |
|-------------|------------|
| Balkendiagramm | Kategorisch, Sequentiell oder Divergierend (je nach Datentyp) |
| Säulendiagramm | Kategorisch, Sequentiell oder Divergierend (je nach Datentyp) |
| Liniendiagramm | Kategorisch, Sequentiell oder Divergierend (je nach Datentyp) |
| Flächendiagramm | Kategorisch, Sequentiell oder Divergierend (je nach Datentyp) |
| Kuchendiagramm / Donut | Kategorisch, Sequentiell oder Divergierend (je nach Datentyp) |
| Streudiagramm | Kategorisch, Sequentiell oder Divergierend (je nach Datentyp) |
| Karten | Kategorisch, Sequentiell erweitert (050–900) oder Divergierend |
| Baumdiagramm | Kategorisch, Sequentiell oder Divergierend (je nach Datentyp) |
| Boxplot | Kategorisch, Sequentiell oder Divergierend (je nach Datentyp) |
| Rasterdiagramm | Kategorisch, Sequentiell oder Divergierend (je nach Datentyp) |
| Heatmap | **Nur Divergierend** |
| Radardiagramm | Kategorisch, Sequentiell oder Divergierend (je nach Datentyp) |
| Tornadodiagramm | **Nur Divergierend** |
| Lollipop-Diagramm | Kategorisch, Sequentiell oder Divergierend (je nach Datentyp) |

---

## 8. Schnellreferenz: Diagrammtyp-Auswahl nach Anwendungszweck

| Anwendungszweck | Empfohlene Diagrammtypen |
|----------------|--------------------------|
| Vergleich von Kategorien | Balkendiagramm, Säulendiagramm, Lollipop-Diagramm |
| Zeitlicher Verlauf / Trends | Liniendiagramm, Flächendiagramm |
| Teil-Ganzes-Beziehung | Kuchendiagramm (max. 6 Teile), Donutdiagramm (max. 6 Teile), Baumdiagramm, Rasterdiagramm |
| Verteilung von Daten | Boxplot, Streudiagramm |
| Korrelation zweier Variablen | Streudiagramm, Heatmap |
| Geografische Daten | Choroplethen-Karte, Symbolkarte mit Punkten, Symbolkarte mit Kreisen |
| Vergleich zweier gegenüberliegender Kategorien | Tornadodiagramm |
| Multivariate Vergleiche | Radardiagramm |
| Positive und negative Werte | Divergierendes Balken-/Säulendiagramm, Divergierende Choroplethen-Karte |
| Hohe Werte mit vielen Kategorien | Lollipop-Diagramm (statt Balkendiagramm) |
| Fortschritt / Prozentanzeige | Rasterdiagramm |
---

## 9. Farbzuordnung Departemente der Stadt Winterthur

**Zweck:** Konsistente Farbkodierung der 7 Departemente und der Stadtkanzlei über alle Visualisierungen hinweg (Dashboards, Berichte, Präsentationen).

**Regeln:**
- Jedes Departement hat eine feste kategorische Hauptfarbe und eine zugehörige sequentielle Skala.
- Die Hauptfarbe wird auf der Departement-Ebene verwendet (z. B. Balkendiagramm mit allen Departementen).
- Die sequentielle Skala wird innerhalb eines Departements verwendet, um untergeordnete Einheiten (Bereiche, Ämter, Produktegruppen) zu unterscheiden.
- Die Stufenauswahl innerhalb der sequentiellen Skala richtet sich nach §3.9 (Empfohlene Skalenauswahl).

### 9.1 Zuordnungstabelle

| Departement                          | Kat. Nr. | Hauptfarbe (HEX) | Sequentielle Skala        |
|--------------------------------------|----------|-------------------|---------------------------|
| Departement Präsidiales              | 01       | #CB2512           | Rot (§3.1)                |
| Departement Finanzen                 | 02       | #A554C7           | Violett (§3.2)            |
| Departement Bau und Mobilität        | 03       | #1592C0           | Blau (§3.3)               |
| Departement Sicherheit und Umwelt    | 04       | #0C6974           | Petrol (§3.4)             |
| Departement Schule und Sport         | 05       | #1E9B6F           | Grün (§3.5)               |
| Departement Soziales                 | 06       | #F1A79F           | Rot hell (§3.1, Stufen 100–700) |
| Departement Technische Betriebe      | 08       | #C07915           | Orange (§3.7)             |
| Behörden und Stadtkanzlei            | 09       | #BD377A           | Pink (§3.8)               |

### 9.2 Anwendungsbeispiel

**Visualisierung: Investitionsplanung nach Departementen**

- Auf der obersten Ebene (Vergleich aller Departemente) erhält jedes Departement seine Hauptfarbe.
- Beim Drill-Down in ein Departement (z. B. «Bau und Mobilität») werden die untergeordneten Bereiche (Tiefbauamt, Vermessungsamt, Baupolizeiamt, Amt für Städtebau) in der sequentiellen Blau-Skala dargestellt.
- Die Stufenauswahl richtet sich nach der Anzahl der Bereiche: bei 4 Bereichen werden die Stufen 100, 300, 500, 700 verwendet (gemäss §3.9).

### 9.3 Sequentielle Skala «Dep. Soziales» (Sonderfall)

Das Departement Soziales verwendet die kategorische Farbe 06 (Rot 100, #F1A79F) als Hauptfarbe, welche eine helle Pastellfarbe ist. Die zugehörige sequentielle Skala wurde separat abgeleitet, da die offizielle Rot-Skala (§3.1) bereits vom Departement Präsidiales belegt ist.

| Stufe | HEX     |
|-------|---------|
| 100   | #F0A59D |
| 200   | #ED8377 |
| 300   | #EA6051 |
| 400   | #E83D2B |
| 500   | #D62714 |
| 600   | #B21E0E |
| 700   | #8E170A |

**Hinweis:** Diese Skala liegt im gleichen Farbton (H≈6°) wie die offizielle Rot-Skala, ist aber eigenständig abgeleitet, um Verwechslungen zu vermeiden. Die Hauptfarbe (#F1A79F) des Departements Soziales entspricht Stufe 100.
