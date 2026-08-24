# NEXT by Meyer & Denker – Landingpage

Einfache, statische Landingpage zur Bewerbung der Workshop-Reihe **NEXT** für Young Professionals.
Reines HTML/CSS, kein Build-Schritt, keine Abhängigkeiten. Gehostet bei **Strato**
(Domain: **meyerdenker.de**), automatisch veröffentlicht per **GitHub Actions**.

## Dateien

| Datei | Inhalt |
|-------|--------|
| `index.html` | Komplette Landingpage (alle Inhalte) |
| `impressum.html` | Impressum (§ 5 TMG) |
| `datenschutz.html` | Datenschutzerklärung (DSGVO) |
| `styles.css` | Design & Layout (Farben zentral über CSS-Variablen) |
| `assets/` | Logo, Gründerinnen-Porträts und selbst gehostete Inter-Schrift (`assets/fonts/`) |
| `.github/workflows/deploy.yml` | Automatischer SFTP-Upload zu Strato bei Push auf `main` |

## Lokal ansehen

`index.html` einfach im Browser öffnen (Doppelklick). Kein Server nötig.

## Veröffentlichen / Pflegen (Strato, automatisch)

Ablauf im Alltag: **hier ändern → committen → `git push` auf `main`** → die GitHub Action lädt
die geänderten Dateien automatisch per SFTP (Port 22) zu Strato hoch. Fertig.

### Einmalige Einrichtung

1. **Strato – FTP/SFTP-Zugang anlegen:** Im Strato-Kundenbereich einen (S)FTP-Benutzer erstellen
   (oder den vorhandenen nutzen). Notieren: **Server/Host**, **Benutzername**, **Passwort**.
2. **Domain zuweisen:** In der Strato-Domainverwaltung **meyerdenker.de** auf den Upload-Ordner
   zeigen lassen (Webspace-Root `/` oder ein Unterordner) und **SSL/Let's Encrypt** aktivieren.
3. **GitHub-Zugangsdaten hinterlegen** unter *Repo → Settings → Secrets and variables → Actions*:
   - **Secrets:** `STRATO_FTP_SERVER`, `STRATO_FTP_USERNAME`, `STRATO_FTP_PASSWORD`
   - **Variable:** `STRATO_REMOTE_DIR` = Zielordner im Webspace (z. B. `/`)
4. **Auf `main` bringen:** Diesen Branch nach `main` mergen. Danach läuft der Deploy bei jedem Push
   automatisch (Fortschritt unter *Repo → Actions → „Deploy to Strato“*).

> Der Workflow lädt nur die Web-Dateien hoch; `README.md`, `.github/` und Git-Interna werden
> ausgeschlossen.

## Inhalte anpassen

Alle Texte stehen direkt in `index.html` – einfach im Editor ändern.

- **Farben** ändern: Variablen ganz oben in `styles.css` (`:root { ... }`).
- **Kontakt-E-Mail**: im HTML nach `info@meyerdenker.de` suchen und ersetzen.
- **Porträts**: `assets/founder-2.png` (Marina Meyer) und `assets/founder-1.png` (Carina Denker).

## Noch zu ergänzen (vor dem finalen Livegang)

- **Impressum** und **Datenschutzerklärung** – für gewerbliche Websites in Deutschland
  rechtlich erforderlich. Aktuell im Footer als Platzhalter markiert.
- Optional: konkrete Termine / Verfügbarkeit.

---

Design, Farben (`#008C8C`, `#0F2F36`, `#F4F1EC`, `#CE7359`) und Inhalte wurden aus der
Marken-Präsentation abgeleitet. Schrift: **Inter** (selbst gehostet unter `assets/fonts/`,
kein externes Font-CDN – DSGVO-freundlich).
