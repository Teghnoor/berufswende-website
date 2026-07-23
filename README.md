# Berufswende — Landingpage

Neuaufbau der Seite [berufswende.de](https://berufswende.de). Eine self-contained `index.html`, kein Build, keine Abhängigkeiten außer Google Fonts.

## Ausrichtung

Die Seite folgt dem Aufbau einer modernen Sales-Landingpage: **VSL groß und zentriert direkt unter dem Hero**, darunter Problem/Lösung, Handwerk, Ablauf, Beweis, Passung und Abschluss. Referenz für die Design-Sprache war master-circle.de.

**Vorgängerfassung („Cinematic Dusk", Commit `bd3f23b`) ist verworfen.** Sie war typografisch literarisch (Cormorant Garamond), sehr leer und hat das VSL als Nebenelement behandelt.

## Design-System

**Typografie** — keine Serif auf der Seite.

- `Inter Tight` für Headlines: 700/800, `letter-spacing: -.035em`, bis ~4,9rem
- `Inter` für Fließtext
- Headline-Muster: erste Zeile weiß, zweite Zeile in Kupfer

**Farbe** — dunkler und kontrastreicher als zuvor, damit Karten Tiefe bekommen.

- Grund `#050E10`, Flächen `#081619` / `#0B1E21`
- Kupfer `#D9975F` als einziger Akzent: Kicker-Dots, Akzentzeile, primärer CTA, Glows
- Karten `rgba(255,255,255,.022)` auf `1px` Border, `16px` Radius
- Rollen-Tints: Ausschlusskriterien warm-rötlich, Lösungskarten kupfern

**Tiefe und Bewegung** tragen die Qualität, weil es kein Bildmaterial gibt: Karten-Hover mit Lift, gestaffeltes Scroll-Reveal, radiale Glows hinter Hero und VSL, sehr feines Korn. Alles respektiert `prefers-reduced-motion`.

## Struktur

| # | Sektion | Inhalt |
|---|---|---|
| 0 | Topbar | Vorgespräch kostenlos und unverbindlich |
| 1 | Header | sticky, Wortmarke + Nav + CTA, Burger unter 960px |
| 2 | Hero | zentriert, zweifarbige Headline, zwei CTAs, Trust-Dots |
| 3 | **VSL** | groß, zentriert, volle Contentbreite |
| 4 | Worum es geht | 3× Problem + 1× Lösung als 2×2-Grid |
| 5 | Was du lernst | vier Feature-Karten mit Icons |
| 6 | Ablauf | vier Etappen als vertikale Timeline |
| 7 | Zahlen | drei Stat-Boxen — **Werte offen** |
| 8 | Stimmen | drei Zitat-Karten — **Inhalte offen** |
| 9 | Passung | vier Ausschlusskriterien, danach die Einladung |
| 10 | Wer dahinter steht | ohne Foto, mit ehrlichem Hinweis |
| 11 | Was noch fehlt | Transparenz über offene Belege |
| 12 | Fragen | FAQ, eine Antwort zur Zeit |
| 13 | Vorgespräch | drei Schritte + Formular |

## Grundsatz für alle künftigen Änderungen

Die Marke positioniert sich ausdrücklich darüber, nichts Unbelegtes zu behaupten. Deshalb hat diese Seite bewusst **keine** Scarcity-Zeile („nur noch X Plätze"), keine erfundenen Kennzahlen, keine Presse-Logos und keine Erfolgs- oder Einkommensversprechen — obwohl die Referenz genau davon lebt.

Wo Belege fehlen, steht ein sichtbarer Platzhalter (`class="slot"`), kein erfundener Inhalt.

## VSL einhängen

In `index.html` beim Block `▼▼ VSL EINHÄNGEN ▼▼`:

1. Kommentar auflösen
2. `poster="…"` auf ein Standbild setzen
3. `<source src="…">` auf die Videodatei setzen
4. den `<div class="vsl-empty">` darunter löschen

Autoplay stumm, der runde Unmute-Button und das Pausieren außerhalb des Sichtfelds laufen dann von selbst. Beim Einschalten des Tons springt das Video auf Anfang und bekommt die nativen Controls.

## Platzhalter befüllen

- **Zahlen:** in den drei `.stat`-Boxen `.stat-v` (Wert) und `.stat-l` (Bezeichnung) setzen, dann `slot` aus der Klasse entfernen
- **Stimmen:** in den drei `.quote`-Karten Zitat und Name eintragen, dann `slot` entfernen

## Offen vor dem Livegang

- **VSL** einhängen
- **Formular** verschickt nichts — Empfänger, Übermittlungsweg und Datenschutzerklärung fehlen
- **Anbieter-Person**: Foto und Name in „Wer dahinter steht", Hinweistext dort entfernen
- **Impressum und Datenschutz** verlinken
- **Logo-Original** als SVG einsetzen (aktuell als Inline-SVG nachgebaut)

## Lokale Vorschau

```bash
python3 -m http.server 8899
# http://localhost:8899
```
