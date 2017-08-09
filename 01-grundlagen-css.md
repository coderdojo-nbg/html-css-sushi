# CSS – Cooler Look für die Seite
## Was ist CSS?
CSS bedeutet **Cascading Style Sheet**, und damit kannst du deine Website, die du mit Hilfe der HTML-Sushi-Karte erstellt hast, noch etwas schöner gestalten. CSS sind sozusagen Formatvorlagen — **Regeln** —, die du für jede Website individuell anlegen kannst. Dadurch sieht jede Website anders aus.

Du findest bestimmt auch, dass die Website, wie sie jetzt aussieht, nicht besonders cool und interessant wirkt. Es wäre bestimmt super, wenn man die Farben oder die Schriftgrößen ändern könnte. Dir fallen bestimmt noch ganz viele andere Dinge ein, die du auf der Seite verändern möchtest.

Aber fangen wir erst mal damit an, wie eine CSS-Regel aufgebaut ist.

## CSS-Regeln: Struktur und Aufbau

Der allgemeine Aufbau einer CSS-Regel sieht so aus:

```css
Selektor {
    Eigenschaft1: Wert1;
    Eigenschaft2: Wert2;
}
```

Ein **Selektor** ist das jeweilige HTML-Element z.B `<h1>`, welches ich verändern möchte. Es gibt verschiedene Arten von Selektoren, darunter:

1. Solche, die sich auf ein **HTML-Element** beziehen, z.B. `<h1>`, `<p>` oder `<ul>`
2. Solche, die sich auf das **Klassenattribut** von HTML-Elementen beziehen (z.B. `class="active"`)
3. Solche, die sich auf die **eindeutige ID** eines HTML-Elements beziehen (`id="unique-element"`)

CSS-Klassen werden wir später noch näher erläutern. ID-Selektoren können problematisch sein und die Praxis zeigt, dass man alles, was man damit erreichen kann, auch mit CSS-Klassen umsetzen kann — du benötigst ID-Selektoren also nicht.

**Eigenschaften**, die du per CSS verändern kannst, sind z.B. die Farbe (`color`) oder Schriftgröße (`font-size`) eines HTML-Elements.

Der **Wert** ist dann z.B. der Farbwert (z.B. `green` oder `#009900`) oder die Größenangabe (z.B. `16px`).

Wenn ich also alle `<h1>`-Überschriften in meiner Website grün einfärben möchte, dann muss ich folgende CSS-Regel formulieren:

```css
h1 {
    color: green;
}
```

`h1` ist hier der Selektor, `color` ist die Eigenschaft und `green` der Wert.

## Wie kommt das CSS in meine HTML-Datei?

### Externe Stylesheets

Es gibt verschiedene Möglichkeiten, eine CSS-Datei in ein HTML-Dokument einzubinden. Der beste und professionellste Weg ist eine eigene externe CSS-Datei. Dazu legst du im Editor deiner Wahl eine neue Datei an und speicherst diese z.B. unter dem Namen `styles.css` im gleichen Verzeichnis wie deine HTML-Datei.

Als nächstes schreiben wir eine CSS-Regel in die Datei, z.B. die oben gezeigte zum Einfärben aller `<h1>`-Überschriften:

```css
h1 {
  color: red;
}
```

Abspeichern nicht vergessen! 😉

Dann müssen wir unsere CSS-Datei noch in die HTML-Datei einbinden. Dazu ergänzt du ein `<link>`-Element an einer beliebige Stelle im `<head>`-Bereich deiner HTML-Datei:

```html
<head>
    <!-- Hier wird die CSS-Datei eingebunden -->
    <link rel="stylesheet" type="text/css" href="styles.css" />
</head>
```

Speichern wider nicht vergessen! Wenn du alles richtig gemacht hast und du dir die Seite im Browser ansiehst, sollte die Überschrift jetzt grün sein.

## Verschiedene Styles

Es gibt natürlich viele verschiedene Eigenschaften, die ein Text haben kann. Wir können z.B. auch die Textgröße ändern — wir nutzen dafür nun beispielhaft das Element `<p>` für Absätze in deiner HTML-Datei. Wir wollen nun die Schrift in diesen Absätzen etwas größer machen. Dazu brauchen wir die CSS-Eigenschaft `font-size`.

Ergänze folgende Regel in deiner CSS-Datei:

```css
p {
    font-size: 16px;
}
```

Der Wert `16px` ist die Größenangabe für die Schrift und `px` ist dabei die Maßeinheit (Pixel). Speichere deine CSS-Datei ab und schau dir die HTML-Datei im Browser an.

### Weitere Textformate

Wie wäre es mit einer anderen Schriftstärke? Diese können wir mit `font-weight` festlegen. Ergänze folgendes in deiner CSS-Datei:

```css
p {
    font-size: 16px;
    font-weight: bold;
}
```

Speichere die Datei und sieh dir das Ergebnis im Browser an: Nun müssten alle Absätze fett erscheinen. Hier eine kleine Liste von möglichen Textformaten:

* `font-weight`: Schriftstärke ändern (siehe oben)
  Mögliche Werte: `lighter`, `light`, `normal`, `bold`, `bolder` oder alternativ Zahlenwerte zwischen `100` und `900` (in 100er-Schritten)
* `font-family`: Schriftart ändern
  Mögliche Werte: alle Schriften, die auf dem Computer installiert sind
    ```css
    p {
        font-family: Verdana, Arial;
    }
    ```
* `font-style`: Schriftstil ändern
  Mögliche Werte: `italic`, `oblique`, `normal`
    ```css
    p {
        font-style: italic;
    }
    ```
* `text-decoration`: einen Text dekorieren, z.B unterstreichen
    Mögliche Werte: `underline`, `overline`, `line-through`, `none`
    ```css
    p {
        text-decoration: underline;
    }
    ```

Damit lässt sich schon einiges gestalten. Probier es einfach mal aus und tippe verschiedene Textformate in deine CSS-Datei ein. Schau dir die Ergebnisse im Browser an.

## CSS-Klassen bilden

Mit den HTML-Elementen und passenden CSS-Regeln kannst du in deiner Website schon ziemlich viel verändern und formatieren. Aber wenn du eine CSS-Regel z.B für das `<p>`-Element einfügst, dann hast du sicherlich bemerkt, dass dann alle `<p>`-Absätze diese Formatierungen übernehmen. Aber wie kann man nur einen speziellen Absatz z.B. fett gestalten oder mit einer anderen Farbe einfärben?

Dafür brauchen wir **CSS-Klassen**. Mit Klasse ist keine Schulklasse gemeint, sondern damit kannst du eine Formatierung, die du einmal erstellt hast, auf mehrere beliebige Elemente anwenden, indem du ihnen das passende Klassenattribut gibst. Der englische Begriff dafür ist **class**.

Ein Klassennamen wird gebildet, indem man sich einen möglichst aussagekräftigen, zusammenfassenden Namen für die Formatierung ausdenkt und diesen den gewünschten HTML-Elementen als `class`-Attribut gibt. Verwende für CSS-Klassennamen am besten immer nur Kleinbuchstaben, wenn es sein muss Ziffern und den Bindestrich.

In deiner HTML-Datei färben wir nun die Schrift in einem bestimmten Absatz grün. Folgendes musst du dazu ergänzen:

```html
<p class="gruen">
    Hier steht dein Text, der grün werden soll.
</p>
```

In der CSS-Datei formulieren wir nun eine Regel, die einen Klassenselektor benutzt:

```css
.gruen {
    color: green;
}
```

Wie du siehst, beginnen Klassenselektoren mit einem Punkt `.`, gefolgt von dem Klassennamen, den du dir ausgedacht hast. Schau dir das Ergebnis im Browser an. Natürlich speichern nicht vergessen.

Mit den Klassen hast du also die Möglichkeit, in jedem gewünschten Element die Schrift oder Farbe oder beides zu verändern. Du musst dazu nur das Klassenattribut beim HTML-Element ergänzen.

## Verkettete Selektoren

Ein CSS-Selektor kann sich auch aus mehreren einzelnen Selektoren zusammensetzen. Z.B. kann ich aus mehreren Absätzen `<p>` nur bestimmte Elemente auswählen, indem ich die passenden Selektoren verkette.

Ein Beispiel: Ich habe zwei Absätze `<p>` und möchte nur die Listenpunkte des zweiten Absatzes mit der Klasse `gruen` auswählen. Hier der HTML-Code:

```html
<p>
     Hier steht ein toller Text und eine schöne Liste:
     <ul>
        <li>Listenpunkt1</li>
        <li>Listenpunkt2</li>
    </ul>
</p>
<p class="gruen">
     Hier steht ein toller grüner Text und eine schöne Liste:
     <ul>
        <li>Listenpunkt1</li>
        <li>Listenpunkt2</li>
    </ul>
</p>
```

Die CSS-Regel lautet für die Listenpunkte im zweiten Absatz nun so:

```css
p.gruen ul li {
   color: red;
}
```

Gesprochen lautet diese Regel so viel wie: "Wähle alle `<li>`-Elemente aus, die in einem `<ul>`-Element liegen, das in einem `<p>`-Element mit der Klasse `gruen` liegt, und färbe seine Schrift rot ein.". Am besten, du liest verkettete CSS-Selektoren von rechts nach links, um sie schnell zu begreifen. Probier es doch einfach aus und tippe den Code in deine HTML- und CSS-Datei.

## Noch mehr CSS-Regeln

Es gibt natürlich noch ganz viele CSS-Eigenschaften, die man in seiner Website verwenden kann. Z.B. möchtest du vielleicht die Abstände zwischen zwei Absätzen ändern oder den Text einrücken. Dafür gibt es folgende CSS-Anweisungen:

* `margin`: Außenabstände
* `padding`: Innenabstände

Bei beiden Eigenschaften kann man den Abstand rundherum auf denselben Wert setzen oder jede Seite einzeln ändern (also oben, rechts, unten, links):
* `margin-top`, `margin-right`, `margin-bottom`, `margin-left`
* `padding-top`, `padding-right`, `padding-bottom`, `padding-left`

Ergänze folgende Anweisung in deiner CSS-Datei:

```css
.gruen {
    color: green;
    padding-left: 20px;
    margin-top: 50px;
}
```

Abspeichern und dann schau dir das Ergebnis im Browser an. Wenn alles richtig ist, dann ist der Absatz mit grüner Schrift links weiter eingerückt und hat oben einen größeren Abstand.

In deiner Website befinden sich noch andere Elemente, wie z.B. die Liste `<ul>`. Diese lässt sich auch einrücken, damit deutlich wird, dass es sich um eine Liste handelt. Ergänze folgende Regel in deiner CSS-Datei:

```css
ul {
    padding-left: 30px;
}
```

Wenn du abspeicherst und die HTML-Seite im Browser ansiehst, kannst du sehen, dass die Liste nun links weiter eingerückt ist. Mit diesem Grundwissen kannst du in deiner Website schon einiges schöner gestalten.

Probier es einfach aus. Bei Fragen kannst du dich jederzeit an die Mentoren wenden. Wie wäre es mit einer eigenen kleinen Website? **Viel Spaß dabei!**
