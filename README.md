# Haut Manufaktur Chemnitz — Website

Kompletter Redesign der Website für die **Haut Manufaktur Chemnitz** –
Institut für ästhetische Kosmetik & dauerhafte Haarentfernung
(ein Projekt der amaderm GmbH).

Die Seite ist eine schnelle, moderne, vollständig statische Website
(HTML/CSS/JS, kein Build-Schritt nötig) und kann direkt über **GitHub Pages**
ausgeliefert werden.

## ✨ Features

- **Vollständig responsiv** – optimiert für Desktop, Tablet & Smartphone
- **Premium-Design** – elegante Serifen-Typografie, warme „Manufaktur"-Farbwelt
- **Sanfte Animationen** – Reveal-on-Scroll, animierte Zähler, Marquee, Akkordeon
- **6 Seiten:** Start, Kosmetik & Anti-Aging, Haarentfernung, Preise, Kontakt,
  plus Impressum & Datenschutz
- **Echte Inhalte** – Leistungen, Google-Bewertungen (4,8 ★), Standort mit Karte
- **SEO-optimiert** – Meta-Tags, `sitemap.xml`, `robots.txt`, sprechende Struktur
- **Barrierearm** – semantisches HTML, `prefers-reduced-motion`, Fokus-Stile

## 📁 Projektstruktur

```
.
├── index.html            # Startseite
├── kosmetik.html         # Kosmetik & Anti-Aging
├── haarentfernung.html   # Dauerhafte Haarentfernung
├── preise.html           # Preisübersicht
├── kontakt.html          # Kontakt, Formular & Karte
├── impressum.html        # Impressum (Vorlage – bitte ergänzen)
├── datenschutz.html      # Datenschutzerklärung (Vorlage – bitte ergänzen)
├── css/styles.css        # Komplettes Design-System
├── js/main.js            # Interaktionen (Menü, Scroll, FAQ, Zähler, Formular)
├── assets/favicon.svg    # Favicon / Logo-Mark
├── images/               # Hier echte Fotos ablegen (siehe images/README.md)
├── sitemap.xml, robots.txt
└── .github/workflows/deploy.yml   # Auto-Deploy zu GitHub Pages
```

## 🚀 Veröffentlichen über GitHub Pages

1. Diesen Branch mergen bzw. den Code in den `main`-Branch bringen.
2. Im Repository unter **Settings → Pages** als Quelle **„GitHub Actions"** wählen.
3. Der Workflow `.github/workflows/deploy.yml` veröffentlicht die Seite
   automatisch bei jedem Push auf `main`.
4. Die Seite ist danach unter
   `https://<benutzername>.github.io/<repo>/` erreichbar.

### Eigene Domain (haut-manufaktur.com)

Soll die Seite unter der eigenen Domain laufen, in **Settings → Pages →
Custom domain** die Domain eintragen und beim Domain-Anbieter die
entsprechenden DNS-Einträge (CNAME/A-Records) setzen. GitHub legt dann
automatisch eine `CNAME`-Datei an.

## 🖼️ Bilder einbinden

Die Original-Fotos konnten aus der Build-Umgebung heraus nicht heruntergeladen
werden (die Domain ist dort netzwerkseitig gesperrt). Überall, wo ein Foto
hingehört, ist ein eleganter Platzhalter mit dem gewünschten Dateinamen
eingebaut. Anleitung zum Austausch: **[`images/README.md`](images/README.md)**.

## 🔧 Lokal ansehen

Einfach `index.html` im Browser öffnen – oder für saubere Pfade einen kleinen
Server starten:

```bash
python3 -m http.server 8000
# dann http://localhost:8000 öffnen
```

## 📝 Vor dem Live-Gang bitte prüfen

- [ ] Echte Fotos in `images/` ablegen und Platzhalter ersetzen
- [ ] Impressum vervollständigen (Geschäftsführung, USt-IdNr., verantwortliche Person)
- [ ] Datenschutzerklärung an die tatsächlich eingesetzten Dienste anpassen
- [ ] Preise final prüfen (aktuell Richtpreise als Platzhalter)
- [ ] Kontaktformular an ein Backend/E-Mail-Postfach anbinden (aktuell Demo)
- [ ] Google-Bewertungen ggf. um weitere/aktuelle Rezensionen ergänzen

---

© Haut Manufaktur Chemnitz · Ein Projekt der amaderm GmbH
