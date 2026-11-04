# SentinelGuard Website

Offizielle Website für SentinelGuard Antivirus.

## Struktur

```
website/
├── index.html          # Hauptseite
├── css/
│   └── style.css      # Stylesheet
├── js/
│   └── main.js        # JavaScript
└── assets/            # Bilder, Icons (bei Bedarf)
```

## Lokal testen

Öffnen Sie einfach `index.html` in einem Browser, oder nutzen Sie einen lokalen Webserver:

```bash
# Python 3
python -m http.server 8000

# Node.js (mit http-server)
npx http-server
```

Dann öffnen Sie `http://localhost:8000` im Browser.

## Hosting

Die Website kann auf verschiedenen Plattformen gehostet werden:

### GitHub Pages

1. Repo `sg-website` erstellen
2. `website/`-Inhalt in `main`-Branch hochladen
3. Settings → Pages → Source: `main` → Ordner: `/(root)`
4. Website erreichbar unter `https://username.github.io/sg-website`

### Netlify

1. Netlify-Konto erstellen
2. Drag & Drop des `website/`-Ordners in Netlify Dashboard
3. Fertig – Netlify generiert eine URL

### Eigener Webserver

- FTP/SFTP hochladen
- Apache/Nginx konfigurieren
- HTTPS via Let's Encrypt aktivieren

## Anpassungen

### Download-Links aktualisieren

In `index.html` den Windows-Download-Link anpassen:

```html
<a href="https://github.com/Dodovking/sg-updates/releases/download/v1.1.3/SentinelGuard-Setup-1.1.3.exe"
   class="btn btn-primary btn-download">Herunterladen</a>
```

### SHA-256 aktualisieren

Jedes Mal, wenn ein neuer Installer gebaut wird, den SHA-256-Hash in `index.html` aktualisieren:

```html
<p class="download-sha">SHA-256: <code>NEUER_HASH_HIER</code></p>
```

### Release Notes

Release Notes in `index.html` unter `<section class="release-notes">` ergänzen.

### Rechtliche Seiten

Die Links für Impressum, Datenschutz und Lizenz in `index.html` erstellen:

```html
<a href="impressum.html">Impressum</a>
<a href="datenschutz.html">Datenschutz</a>
<a href="lizenz.html">Lizenz (MIT)</a>
```

Dann die entsprechenden HTML-Dateien im `website/`-Ordner erstellen.

## Design

Das Design basiert auf dem SentinelGuard Dark-Theme:

- Hintergrund: `#0f141a` (primär), `#161d27` (sekundär), `#252f3d` (Karten)
- Akzentfarbe: `#3b82f6` (Blau)
- Erfolg: `#22c55e` (Grün)
- Warnung: `#f59e0b` (Orange)
- Gefahr: `#ef4444` (Rot)

Schriftart: Inter (via Google Fonts)

## Responsive

Die Website ist vollständig responsive und funktioniert auf Desktop, Tablet und Mobile.
