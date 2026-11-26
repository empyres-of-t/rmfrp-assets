# Buchmalerei-Bereichstrenner

Die transparenten PNGs verwenden die Sepialinie und die weinroten Ranken des Buchmalerei-Rahmens. Das waagerechte Mittelstück enthält zusätzlich dessen kleine Goldbeeren.

| Teil | PNG-Größe | Anzeige und Platzierung |
|---|---:|---|
| `Waagerecht/links.png`, `Waagerecht/rechts.png` | 112 × 64 px | Je 28 × 16 CSS-px an den äußeren Enden |
| `Waagerecht/linie.png` | 64 × 64 px | 16 CSS-px hoch, waagerecht bis zur Mitte strecken |
| `Waagerecht/mitte.png` | 368 × 64 px | Optionales Mittelornament mit eingebauter Linie, 92 × 16 CSS-px |
| `Senkrecht/oben.png`, `Senkrecht/unten.png` | 64 × 112 px | Je 16 × 28 CSS-px oben und unten |
| `Senkrecht/linie.png` | 64 × 64 px | 16 CSS-px breit, senkrecht zwischen den Enden strecken |

## Waagerecht

Die beiden Endstücke mit je einem gleich langen Linienabschnitt zur Mitte hin verlängern. Die Linien an alle Grafikstücke bündig anschließen. An der Mitte können die Linien zusammentreffen, einen Titel einfassen oder ans Mittelornament anschließen.

- Beim **Titel** links und rechts etwas Luft lassen. Der Titel kann aus echtem Text oder aus einer separaten Schriftgrafik bestehen. Im CSS-Beispiel kann ein längerer Titel umbrechen.
- Das **Mittelornament** bündig zwischen die Linien setzen. Seine Linie ist bereits im PNG enthalten. Ab **148 CSS-px Breite** haben Endstücke und Ornament ausreichend Platz. Bei schmaleren Trennern zeigt das CSS-Beispiel die durchgehende Linie.
- Für die **durchgehende Linie** die beiden Linienabschnitte in der Mitte zusammentreffen lassen. Die Endstücke brauchen insgesamt 56 CSS-px Breite.

## Senkrecht

`oben.png`, `linie.png` und `unten.png` bündig von oben nach unten aneinanderlegen. Ab 56 CSS-px Gesamthöhe füllt die Linie die freie Höhe zwischen den Enden. In einer Grid-Zeile oder einer Flex-Zeile wächst der Trenner im CSS-Beispiel mit der Zeilenhöhe.

## HTML-Beispiele

```html
<link rel="stylesheet" href="Bereichstrenner.css">

<h2 class="buchtrenner-waagerecht buchtrenner-mit-titel">
  <span class="buchtrenner-titel">Fertigkeiten</span>
</h2>

<div class="buchtrenner-waagerecht" role="separator">
  <span class="buchtrenner-mitte" aria-hidden="true"></span>
</div>

<div class="buchtrenner-waagerecht" role="separator"></div>

<div class="buchtrenner-senkrecht" role="separator" aria-orientation="vertical"></div>
```

Die Vorschau ist aus den gelieferten PNGs auf der Ecru-Textur des Büttenbogens zusammengesetzt.
