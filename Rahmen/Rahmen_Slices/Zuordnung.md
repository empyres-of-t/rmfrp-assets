# Buchmalerei-Rahmen

Eine einzelne Sepialinie mit weinroten Eckzweigen, kleinen Goldbeeren und transparentem Innenfeld. Die Mittelornamente sitzen auf der jeweiligen Rahmenlinie und werden nach Breite und Höhe unabhängig eingeblendet.

## PNGs und Anzeigegrößen

| Datei | PNG-Größe | Verwendung |
|---|---:|---|
| `Rahmen.png` | 512 × 512 px | Vorlage für CSS `border-image`. Schnittweite 224 Bildpixel pro Seite. Die vier Ecken werden je 56 × 56 CSS-px groß angezeigt. |
| `Ecken/*.png` | Je 224 × 224 px | Dieselben vier Ecken als Einzeldateien. An jeder Ecke 56 × 56 CSS-px belegen. |
| `Kanten/oben.png`, `Kanten/unten.png` | Je 64 × 224 px | Jeweils 56 CSS-px hoch. Nur horizontal auf die freie Breite zwischen den Ecken strecken. |
| `Kanten/links.png`, `Kanten/rechts.png` | Je 224 × 64 px | Jeweils 56 CSS-px breit. Nur vertikal auf die freie Höhe zwischen den Ecken strecken. |
| `Ornamente/oben.png`, `Ornamente/unten.png` | Je 336 × 64 px | Mit 84 × 16 CSS-px über die jeweilige Kantenmitte legen. |
| `Ornamente/links.png`, `Ornamente/rechts.png` | Je 64 × 336 px | Mit 16 × 84 CSS-px über die jeweilige Kantenmitte legen. |

Für einen Aufbau aus Einzeldateien die Ecken und Kanten bündig aneinanderlegen. Die Rahmenlinie verläuft 9,5 CSS-px von der jeweiligen Außenkante entfernt. Die Mittelachse der Ornament-PNG liegt auf dieser Linie. Die Mitte des Textblocks bleibt transparent.

## Beispiel mit CSS

`Rahmen.css` verwendet den zusammengefassten Rahmen und legt die Mittelornamente über die Linien. Die Ecken und Kanten als Einzeldateien stehen für einen eigenen Aufbau zur Verfügung. Das CSS verwendet Container Queries. Ab 248 px Breite erscheinen die Ornamente oben und unten, ab 224 px Höhe links und rechts. Beide Schwellen können in `Rahmen.css` angepasst werden.

```html
<link rel="stylesheet" href="Rahmen.css">
<div class="buchrahmen">
  <div class="buchrahmen-dekor" aria-hidden="true">
    <span class="buchrahmen-ornament buchrahmen-ornament-oben"></span>
    <span class="buchrahmen-ornament buchrahmen-ornament-unten"></span>
    <span class="buchrahmen-ornament buchrahmen-ornament-links"></span>
    <span class="buchrahmen-ornament buchrahmen-ornament-rechts"></span>
  </div>
  Hier steht der Text.
</div>
```

Die Breite kann der umgebende Bereich vorgeben. Die Höhe ergibt sich aus dem Text und dem Innenabstand. 114 CSS-px Mindestbreite und -höhe lassen Platz für die Ecken. Die Vorschau zeigt vier Größen auf dem Ecru-Papier des bestehenden Büttenbogens.
