# Bilder / Fotos einbinden

Aus technischen Gründen (die Egress-Policy der Build-Umgebung blockiert den
Zugriff auf `haut-manufaktur.com`) konnten die Original-Fotos der bestehenden
Website **nicht automatisch** heruntergeladen werden. Die Website funktioniert
trotzdem vollständig – überall dort, wo ein echtes Foto hingehört, ist aktuell
ein elegant gestalteter Platzhalter (mit Verlauf und Dateiname-Label) eingebaut.

## So tauschst du einen Platzhalter gegen ein echtes Foto

1. Lege deine Bilddatei in diesem Ordner `images/` ab und benenne sie exakt so
   wie im Platzhalter angegeben (siehe Liste unten), z. B. `studio-1.jpg`.
2. Öffne die entsprechende HTML-Datei und ersetze den Platzhalter-Block

   ```html
   <div class="ph ph--rose">
     <svg ...></svg>
     <span class="ph__label">Studio · images/studio-1.jpg</span>
   </div>
   ```

   durch ein `<img>`-Tag:

   ```html
   <img src="images/studio-1.jpg" alt="Behandlungsraum der Haut Manufaktur" />
   ```

   Das umgebende `.media-frame` bzw. `.gallery__item` sorgt automatisch für das
   richtige Seitenverhältnis und den Bildzuschnitt (`object-fit: cover`).

## Benötigte Bilder (Dateinamen)

| Datei                    | Verwendung                               |
|--------------------------|------------------------------------------|
| `studio-1.jpg`           | Startseite – „Über uns" (Hochformat)     |
| `haarentfernung.jpg`     | Startseite – Highlight Haarentfernung    |
| `anti-aging.jpg`         | Kosmetik – Anti-Aging                     |
| `kryolipolyse.jpg`       | Kosmetik – Kryolipolyse                   |
| `laser.jpg`              | Haarentfernung – Diodenlaser              |
| `glatte-haut.jpg`        | Haarentfernung – Vorteile                 |
| `galerie-1.jpg` … `-6.jpg` | Startseite – Galerie                    |

## Tipps

- **Format:** JPG oder WebP, möglichst quer/hoch passend zum Slot.
- **Größe:** ca. 1200–1800 px Breite, komprimiert (< 300 KB) für schnelle Ladezeiten.
- **Hero-Bild (optional):** Der Hero-Bereich nutzt derzeit einen edlen Farbverlauf.
  Wer ein Foto möchte, kann in `css/styles.css` unter `.hero__bg-grad` ein
  Hintergrundbild ergänzen: `background-image: url("../images/hero.jpg");`
