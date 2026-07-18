# Webdesign-Landingpage — Stand des codierten Gerüsts

> Zusammenfassung dessen, was in Claude Code gebaut wurde, zur Übernahme in die
> Project Knowledge. Bewusst **name- und logoagnostisch** gebaut: überall
> Platzhalter, Akzentfarbe/Schriften über CSS-Variablen — der Markenkern kann
> später ohne Neubau eingesetzt werden.

## Ablageort
- Repo: `f5yct67kcv-source/Website`, Branch `claude/github-website-business-setup-vg1d53`
- Zwei Seiten: `hero-referenzband.html` (Startseite), `kostenrechner.html` (eigene Rechner-Seite)
- Weitere Dateien: `design-richtung.md` (Marken-/Ton-/Design-Brief §1–13), Original­entwurf `landingpageentwurf.html`, Farbvariante `landingpage-mittelkupfer.html`

## Designsystem (technischer Kurs)
- **Theme:** warmes Fast-Schwarz `#0a0806`, ein Akzent **Kupfer `#dd8e4a`** (Mittelkupfer). Magenta/zweiter Neonton bewusst entfernt.
- **Kupfer als „industrielle Markierung / Leiterbahn", nicht Luxus-Gold:** dünne Hairlines, Rahmen, Eck-Marker, Blueprint-Raster.
- **Schriften:** Space Grotesk (Display), JetBrains Mono (Labels/Technik), Inter (Fliesstext). → *Offen:* Space Grotesk evtl. später gegen eigenständigere Display-Schrift tauschen.
- **Stil:** reduziert, technisch, Interface-Charakter, nüchterne Typo mit einzelnen starken Headlines, kleine Animationen mit Funktion.
- **Alles über CSS-Variablen** (`--accent`, Schriften) → Farb-/Schrift-Wechsel = ein Handgriff.

## Startseite — Sektionen in Reihenfolge
1. **Hero** — Eyebrow live getippt (`individuell programmiert – kein Template`) + blinkender Cursor; Headline **„Sauber gebaut. Nicht zusammengeklickt."**; kurzer Lead; **ein** CTA „Website-Kosten berechnen" → Rechner; Vertrauenszeile (Fixangebot · Domain gehört dir · persönliche Betreuung); dezentes Blueprint-Raster.
2. **Referenzband** — horizontal endlos laufende Logo-Leiste (Graustufe → Hover Farbe/Pause), Rand-Ausblendung. Aktuell: eigenes Projekt (adrianvonarbfilms.ch-Logo als Eigenentwicklung) + klar gekennzeichnete Platzhalter-Logos.
3. **Warum [Markenname]** — Statement: „Kein Agenturapparat. Keine fünf Meetings, kein Angebot über vierzehn Seiten. Hier kommen Konzept, Design und Entwicklung aus einer Hand …" + Signatur „ein Ansprechpartner · vom ersten Entwurf bis zum Launch".
4. **Angebot („Was ich baue")** — **keine Karten**, drei ruhige Zeilen (01/02/03): Landingpage · Firmenwebsite (3–5 Seiten) · Bestehende Website überarbeiten, je ein Satz; Headline „Nicht jede Website braucht gleich viel. Aber jede braucht einen klaren Zweck."; CTA „Projekt einschätzen". **Keine Preise.**
5. **Wer dahintersteht** — Portrait-Platzhalter links (Bild via `object-fit: cover` vorbereitet), Text rechts („Ich bin Adrian. …"), Abschlusszeile „ein Ansprechpartner · kurze Wege · keine Agenturrunde". Nav „über mich" → `#ueber`. Portrait ist auf Texthöhe begrenzt.
6. **Was kostet das? (CTA)** — kompakte, zentrierte Unterbrechung: „Deine Website ist kein Pauschalprodukt. Dein Preis sollte trotzdem kein Geheimnis sein." + Button „Kosten berechnen" → Rechner.
7. **Footer** — Icon + MARKENNAME + Links (Startseite · Kostenrechner · Kontakt · Impressum · Datenschutz) + regionale Tagline + „E-Mail folgt" + „© 2026 MARKENNAME · individuell entwickelt · ohne Baukastensystem".

## Kostenrechner (eigene Seite)
Ablauf: **Intro → 8 Fragen (eine pro Screen, Fortschrittsbalken) → Ergebnis + Kontakt → „So geht es weiter" → FAQ → Footer.**

**Die 8 Fragen:**
1. Was brauchst du? (Landingpage / Firmenwebsite 3–5 / Umfangreiche Firmenwebsite / Bestehende Website modernisieren)
2. Gibt es bereits eine Website? (Neubau / ersetzen / überarbeiten / Inhalte übernehmen) — bei „Ja" **dynamisches, optionales URL-Feld**
3. Bildmaterial vorhanden? — Foto/Video wird **nicht** automatisch bepreist, sondern separat offeriert
4. Texte vorhanden?
5. Google-Dienste (Mehrfachauswahl; Optionen „alles eingerichtet / bitte prüfen / nichts davon" **exklusiv**). **Technisches SEO ist immer inklusive und kostenlos.**
6. Betreuung nach Launch (Mehrfachauswahl; „selbst verwalten" & „beraten werden" exklusiv)
7. Wann live? (u. a. „zu einem bestimmten Datum" → **Datumsfeld, keine Vergangenheit**)
8. Logo & visueller Auftritt

**Ergebnisansicht:** Überschrift „Dein geschätzter Preisrahmen" → **Platzhalter CHF 1'400–1'800** (echte Preislogik noch nicht implementiert) + kompakte Zusammenfassung aller Antworten + **Sonderleistungen** (Foto/Video, umfassendes Branding) als **„individuell zu prüfen"** + Hinweis „Dieser unverbindliche Richtwert basiert auf deinen Angaben. Nach kurzer Prüfung erhältst du ein verbindliches Festpreisangebot." → **Kontaktfelder direkt darunter** (Name / E-Mail / Telefon optional / Bemerkung) → Button „Projekt unverbindlich anfragen". **Preis ist sichtbar, bevor Kontaktdaten kommen.**

**„So geht es weiter":** 4 Schritte (Anfrage senden → Angaben geprüft → kurze Rückmeldung/Klärung → verbindliches Festpreisangebot) + Zeile „Erst prüfen, dann Angebot, dann entscheidest du. Ohne automatische Buchung."

**FAQ:** Accordion, **single-open** (nur eine Antwort offen), 5 Fragen zum Preisrahmen.

## Preis-Politik (bewusst)
- **Kein öffentlicher „ab"-Preis.** Rechner zeigt einen **Rahmen**, verbindliches **Festpreisangebot erst nach Prüfung**.
- Technisches SEO-Grundgerüst immer inklusive/kostenlos.
- Foto/Video & umfangreiches Branding = separat „individuell zu prüfen".
- Aktueller Preis ist **Platzhalter** (1'400–1'800) bis zur echten Kalibrierung über reale Projekte.

## Platzhalter / offene Punkte (bis Markenkern steht)
- **Markenname:** oben „PLATZHALTER" (Nav/Hero), im Footer „MARKENNAME" — später vereinheitlichen.
- **Logo:** `</>`-Icon als Platzhalter.
- **Portrait:** „[ portrait folgt ]" (Layout & Bildfokus vorbereitet).
- **E-Mail / Kontakt / Impressum / Datenschutz:** Platzhalter (`#`, „E-Mail folgt").
- **Echte Preislogik:** noch nicht umgesetzt.
- **Formular-Absenden:** noch nicht angebunden (nur „Danke"-Bestätigung).
- **Schriftwahl:** evtl. später anpassen.

## Was später ein reiner Einsetz-Schritt ist (kein Neubau)
Markenname (Suchen/Ersetzen) · Logo-Datei · Akzentfarbe (eine Variable) · Portraitfoto · echte Preiswerte · Formular-Endpoint.

## Bereits fixierte Marken-Tonalität (aus `design-richtung.md`)
- **Markenkern:** Direkt · Technisch · Verständlich · Unkompliziert (nicht: emotional/luxuriös/nerdig/arrogant).
- **Haltung:** Gegenmodell zur Agentur — „eine Person statt Apparat", ehrlich, kein Baukasten, kein Marketing-Theater.
- **Ton:** trocken, gegen Baukasten/Plugins/Agentursprech — nie gegen den Kunden; auf jede freche Zeile folgt der Nutzen im Klartext.
- **Wiederkehrende Werte:** sauber · ehrlich · direkt · verständlich · individuell · kein Baukasten · kein Bullshit.
