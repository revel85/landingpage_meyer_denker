# NEXT by Meyer & Denker – Landingpage

Einfache, statische Landingpage zur Bewerbung der Workshop-Reihe **NEXT** für Young Professionals.
Reines HTML/CSS, kein Build-Schritt, keine Abhängigkeiten – bereit für **GitHub Pages**.

## Dateien

| Datei | Inhalt |
|-------|--------|
| `index.html` | Komplette Landingpage (alle Inhalte) |
| `styles.css` | Design & Layout (Farben zentral über CSS-Variablen) |
| `assets/` | Logo und Gründerinnen-Porträts |

## Lokal ansehen

`index.html` einfach im Browser öffnen (Doppelklick). Kein Server nötig.

## Veröffentlichen mit GitHub Pages

1. Änderungen committen und pushen.
2. Im Repository: **Settings → Pages**.
3. Unter **Source** „Deploy from a branch“ wählen.
4. Branch auswählen (empfohlen: `main` nach dem Merge) und Ordner **`/root`**, dann **Save**.
5. Nach ~1 Minute ist die Seite erreichbar unter:
   `https://revel85.github.io/landingpage_meyer_denker/`

## Inhalte anpassen

Alle Texte stehen direkt in `index.html` – einfach im Editor ändern.

- **Farben** ändern: Variablen ganz oben in `styles.css` (`:root { ... }`).
- **Kontakt-E-Mail**: im HTML nach `next@meyerdenker.de` suchen und ersetzen.
- **Porträts**: `assets/founder-1.png` (Marina Meyer) und `assets/founder-2.png` (Carina Denker).
  → **Bitte die Zuordnung Name ↔ Foto einmal prüfen** und bei Bedarf tauschen.

## Noch zu ergänzen (vor dem finalen Livegang)

- **Impressum** und **Datenschutzerklärung** – für gewerbliche Websites in Deutschland
  rechtlich erforderlich. Aktuell im Footer als Platzhalter markiert.
- Optional: konkrete Termine / Verfügbarkeit.

---

Design, Farben (`#008C8C`, `#0F2F36`, `#F4F1EC`, `#CE7359`) und Inhalte wurden aus der
Marken-Präsentation abgeleitet. Schrift: **Inter**.
