# Berufswende — Landingpage

Neuaufbau der Seite [berufswende.de](https://berufswende.de). Eine self-contained `index.html`, kein Build, keine Abhängigkeiten außer Google Fonts.

## Warum neu gebaut wurde

Die Bestandsseite ist mit **Manus** erzeugt (`manus-analytics.com`, `manus-runtime` im ausgelieferten HTML). Ein erster Versuch, ihre Inhalte 1:1 zu übernehmen und nur das Layout zu verbessern, hat den Generator-Ton konserviert — Formulierungen wie „Vorgesehener Dokumentationsfokus" oder „belastbare Entscheidung" sind niemandes Sprache.

Diese Fassung übernimmt die **inhaltliche Substanz**, aber keinen einzigen Satz. Alles neu getextet und neu strukturiert.

## Art-Direction: Cinematic Dusk

Dunkel und filmisch statt technisch. Warme Lichtverläufe wie Fensterlicht zur blauen Stunde, feines Filmkorn über der ganzen Seite, Kupfer sehr sparsam als Akzent. Farben aus dem Logo abgeleitet, Schriften Cormorant Garamond + Manrope mit großem Gradkontrast.

**Kein Bildmaterial.** Der VSL oben ist das einzige Medium der Seite und trägt den Hero. Authentizität entsteht hier über Sprache, Layout-Bruch und Bewegung.

## Bewusst nicht verwendet

Diese Bausteine erzeugen zusammen den Template-Eindruck und kommen auf dieser Seite nicht vor:

- Uppercase-Micro-Kicker über jeder Sektion
- Durchnummerierung `01/02/03`, römische Ziffern
- Hairline-Border-Raster als Standard-Container
- Statistik-Leisten mit drei Kennzahlen
- Symmetrische 3er/4er-Kartenraster
- Kursives Akzentwort in jeder Headline — es gibt genau **eines** auf der ganzen Seite

## Struktur

Neun Sektionen, jede mit einem eigenen Layout-Prinzip statt eines wiederholten Skeletts:

| # | Sektion | Prinzip |
|---|---|---|
| 1 | Hero / VSL | Video als Hauptelement, ein Satz, ein CTA |
| 2 | Der Moment davor | reiner typografischer Block ohne Container |
| 3 | Was du lernst | asymmetrische Spalte, Überschrift bricht die Rasterkante |
| 4 | Wie es abläuft | ein durchlaufender Weg mit scroll-getriebener Linie |
| 5 | Für wen das nichts ist | Ausschlusskriterien zuerst |
| 6 | Wer dahinter steht | Platz für die reale Person, offen markiert |
| 7 | Was hier noch fehlt | Transparenz als Absatz, nicht als Statusraster |
| 8 | Fragen | FAQ, eine Antwort zur Zeit |
| 9 | Vorgespräch | Formular |

## Grundsatz für alle künftigen Änderungen

Die Marke positioniert sich ausdrücklich darüber, nichts Unbelegtes zu behaupten. Menschlichere Sprache heißt **nicht** mehr Behauptung: keine erfundenen Zahlen, Referenzen, Biografien, Einkommens- oder Erfolgsversprechen.

## Offen vor dem Livegang

- **VSL** einhängen: `<source>` im `<video id="vsl">` eintragen und `poster` setzen. Play-Button, Overlay und Controls schalten sich dann automatisch um.
- **Formular** verschickt nichts — Empfänger, Übermittlungsweg und Datenschutzerklärung fehlen.
- **Anbieter-Person**: Foto und Name in der Sektion „Wer dahinter steht" ergänzen, Hinweistext dort entfernen.
- **Impressum und Datenschutz** verlinken.
- **Logo-Original** als SVG/PNG einsetzen (aktuell als Inline-SVG nachgebaut).

## Lokale Vorschau

```bash
python3 -m http.server 8899
# http://localhost:8899
```
