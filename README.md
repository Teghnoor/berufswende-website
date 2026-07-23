# Berufswende — Landingpage (Redesign)

Neuaufbau der Seite [berufswende.de](https://berufswende.de). Inhalte und Platzhalter der Bestandsseite wurden **1:1 übernommen** — verändert wurden ausschließlich Aufbau, Hierarchie und visuelle Umsetzung.

## Stack

Eine einzelne, self-contained `index.html`. Kein Build, kein Framework, keine Abhängigkeiten. Einzige externe Ressource: Google Fonts (Cormorant Garamond + Manrope — dieselben Schriften wie auf der Bestandsseite).

## Was sich gegenüber der Bestandsseite geändert hat

**Struktur**

- Die sechs leeren Nachweis-Kacheln standen bisher direkt unter dem Hero — die erste Aussage der Seite war damit „wir haben noch nichts". Sie sind jetzt in die Sektion **Transparenz** verschoben.
- An ihrer Stelle steht eine Prinzipien-Leiste mit den drei belegbaren Aussagen der Marke: `1:1` · `IV` · `0 Erfolgsversprechen`.
- **Trust-Logos** und **Stimmen** waren zwei getrennte Sektionen voller Platzhalter. Beide sind jetzt unter *„Nachweise, die wirklich belegt sind"* gebündelt: offene Nachweisplätze, vorgesehene Falldokumentationen, Haltungs-Statement. Dieselben Platzhalter — aber als Beleg für die Arbeitsweise statt als Leerstelle.
- **Methodik** rückt direkt hinter „Warum jetzt", weil sie den eigentlichen Substanzblock bildet.
- Navigation von 4 auf 6 Punkte erweitert (bisher waren nur 4 von 11 Sektionen erreichbar).
- Reihenfolge: Hero → Warum → Methodik → Eignung → Über uns → Transparenz → Redaktion → Fragen → Vorgespräch.

**Gestaltung**

- Farbwelt konsequent aus dem Logo abgeleitet: Petrol, Kupfer, Sage, Bone.
- Heller/dunkler Bandwechsel als Lesarhythmus statt durchgehend dunkler Fläche.
- Hairline-Raster statt Kartenkästen; Serif-Ziffern und römische Zahlen als Struktursignal.
- Kompass-Stern aus dem Logo als Inline-SVG (Header, Footer, Favicon, Bildplatzhalter).
- VSL-Platz mit sauberem Rahmen ohne überlappende Boxen; Bildplatzhalter ohne Stockfoto — konsistent zur Aussage, nichts Unbelegtes zu zeigen.
- Scroll-Reveal, Lesefortschritts-Balken, aktiver Nav-Punkt, Mobile-Drawer, FAQ-Akkordeon.
- `prefers-reduced-motion` respektiert, Skip-Link, Fokus-Ringe, kein horizontaler Overflow.

## Offen vor dem Livegang

- Formular ist eine Demo ohne Datenübermittlung — Empfänger, Übermittlungsweg und Datenschutzerklärung fehlen.
- Impressum und Datenschutz sind nicht verlinkt.
- Logo-Original als SVG/PNG einsetzen (aktuell als Inline-SVG nachgebaut).
- VSL, Bildmaterial, Anbieterbiografie, Nachweise und Falldokumentationen nach Freigabe ergänzen.

## Lokale Vorschau

```bash
python3 -m http.server 8899
# http://localhost:8899
```
