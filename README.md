# Sam Plett — Immobilien Website

Unterseite `samplett.de/immobilien` — statische HTML-Seite mit Pipedrive-Anbindung.

## Struktur

```
/
├── index.html          # Hauptseite (93 KB)
├── images/
│   ├── logo.png        # Sam Plett Logo
│   ├── sam-hero.jpg    # Hero Portrait (dark studio)
│   ├── sam-outdoor.jpg # Outdoor mit Gebäude
│   ├── sam-desk.jpg    # Am Schreibtisch
│   ├── sam-speaking.jpg # Sprechend/gestikulierend
│   ├── sam-glass.jpg   # Glastisch-Reflexion (Quote BG)
│   ├── sam-daughter.jpg # Mit Tochter (Quote BG)
│   ├── sam-side.jpg    # Seitenportrait (Team-Sektion)
│   ├── interior.jpg    # Apartment Interior
│   └── tr-*.jpg        # Track Record Gebäudefotos
└── README.md
```

## Pipedrive-Anbindung

Das Kontaktformular sendet direkt an die Pipedrive API:
- Neue **Person** wird angelegt (Name, Email, Telefon)
- Neuer **Deal** in Pipeline "Immo Kunden" → Stage "Lead Organisch"
- **Note** mit vollständiger Nachricht wird am Deal hinterlegt

API-Token in `index.html` Zeile suchen: `var PD_TOKEN = '...'`

## GitHub Pages aktivieren

1. Repository → Settings → Pages
2. Branch: `main`, Folder: `/`
3. URL: `https://[username].github.io/[repo-name]/`

## Deployment auf samplett.de

Die Dateien können direkt in den WordPress-Ordner unter `/wp-content/immobilien/` hochgeladen werden
oder als eigenständige Route via `.htaccess` eingebunden werden.
