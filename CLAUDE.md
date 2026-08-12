# CLAUDE.md — Webdesign-Business (Landingpage + Kostenrechner)

Projektkontext für neue Sessions. **Zuerst lesen:**
`design-richtung.md` (Marken-/Ton-/Design-Brief §1–13) und
`code-stand-zusammenfassung.md` (vollständiger Stand des Gerüsts).

## Was das ist
Eigene Website fürs Webdesign-Angebot einer Person (nicht Agentur). Bewusst
klein, direkt, technisch, ehrlich. Gegenmodell zur Agentur, kein Baukasten,
kein Marketing-Theater.

## Dateien
- `hero-referenzband.html` — **Startseite**: Hero → Referenzband → Warum → Angebot → Wer dahintersteht → „Was kostet das?"-CTA → Footer
- `kostenrechner.html` — **eigene Rechner-Seite**: Intro → 8 Fragen → Ergebnis + Kontakt → „So geht es weiter" → FAQ → Footer
- `design-richtung.md` — Marken-/Ton-/Design-Brief (§1–13, verbindlich)
- `code-stand-zusammenfassung.md` — Detailstand jeder Sektion + Rechnerlogik
- `landingpageentwurf.html` / `landingpage-mittelkupfer.html` — frühere Entwürfe (Archiv)
- `Webdesign_Projekt.skill` — Projekt-Skill (ZIP)

## Goldene Regeln (nicht brechen ohne Rückfrage)
1. **Name-/logoagnostisch bleiben.** Markenname/Logo sind NICHT final. Platzhalter:
   `PLATZHALTER` (Nav/Hero), `MARKENNAME` (Footer), `</>`-Icon, `[ portrait folgt ]`,
   „E-Mail folgt". Keinen Namen/kein Logo erfinden.
2. **Ehrlichkeit (§4/§11).** Keine erfundenen Zahlen/Werte. Kein öffentlicher
   „ab"-Preis. Rechner zeigt einen **Rahmen**; verbindliches Festpreisangebot erst
   nach Prüfung. Aktueller Preis ist **Platzhalter CHF 1'400–1'800** (echte
   Preislogik noch offen).
3. **Ein Akzent.** Kupfer `#dd8e4a` über CSS-Variable `--accent`. Kupfer als
   industrielle Markierung/Leiterbahn, nicht Luxus-Gold. Kein zweiter Neon-Ton.
4. **Ton (§5).** Trocken, direkt; Witz gegen Baukasten/Agentursprech, nie gegen
   den Kunden; auf jede freche Zeile folgt der Nutzen im Klartext.
5. **Keine KI-Template-Optik.** Vorsicht mit generischen Tells (siehe unten).

## Designsystem (Quick-Ref)
- Fast-Schwarz `#0a0806`, Text `#efeae4`, Akzent `#dd8e4a`.
- Schriften: Space Grotesk (Display), JetBrains Mono (Labels/Technik), Inter (Body) — via Google Fonts.
- Reduziert, technisch, Interface-Charakter, Hairlines, Blueprint-Raster.
- `:focus-visible` global gesetzt; `prefers-reduced-motion` respektiert.

## Offene Punkte
- Echte **Preislogik** kalibrieren (statt Platzhalter).
- **Markenidentität** (Name, Wortmarke, Logo, Farbwelt) — kommt aus einem separaten Brand Sprint; danach hier in einem Durchgang einsetzen.
- **Formular-Absenden** real anbinden (aktuell nur „Danke"-Bestätigung).
- **Accessibility-Lücken:** Formularfelder im Rechner brauchen `<label>`/`aria-label` + `autocomplete`/`name`; `aria-live` für Wizard-/Ergebniswechsel; Inline-Fehler statt `alert()`; `color-scheme: dark` + `theme-color`; Skout/Skip-Link; `<img>` mit `width`/`height`.
- **Bekannte KI-Optik-Hebel** (falls „ent-KI-en" gewünscht): Space-Grotesk-Display tauschen; Mono-/Terminal-Motive ausdünnen (eins pro Seite statt pro Sektion); echtes Portraitfoto einsetzen; `01/02/03`-Nummerierung im Angebot überdenken.

## Arbeitsweise / Konventionen
- Reiner HTML/CSS/JS, **kein Framework, kein Build, kein CMS**. Jede Seite ist eine eigenständige Datei.
- Vor dem Bauen einer Sektion die Checkliste in `design-richtung.md` §9 durchgehen.
- Änderungen committen & pushen (dieser Branch). Live-Vorschau via
  `https://htmlpreview.github.io/?<raw-URL der Datei>`.
- CTAs Startseite → `kostenrechner.html`; „über mich" → `#ueber`.
