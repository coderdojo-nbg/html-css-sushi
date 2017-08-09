# CSS – Cooler Look für die Seite
## Was ist CSS?
CSS bedeutet Cascading Style Sheet und damit kannst du deine Webseite, die du mit Hilfe der SushiCard HTML erstellt hast noch etwas schöner gestalten. CSS sind sozusagen Formatvorlagen für deine Seite, die du für jede Seite individuell anlegen kannst. Dadurch sieht jede Seite anders aus.

Du findest bestimmt auch, dass die Webseite, wie sie jetzt aussieht nicht besonders cool und interessant wirkt. Es wäre bestimmt super, wenn man die Farben ändern könnte oder  die Schriftgrößen. Dir fallen bestimmt noch ganz viele andere Dinge ein, die du auf der Seite verändern möchtest.

Aber fangen wir erst mal damit an, wie eine CSS-Angabe aufgebaut ist. 

## CSS-Angaben: Struktur und Aufbau

Der allgemeine Aufbau einer CSS-Angabe lautet so:

```css
Selektor {
	Eigenschaft1: Wert;
	Eigenschaft2: Wert;
}
```

Ein Selektor ist das jeweilige HTML-Element z.B h1, welches ich verändern möchte.
Es gibt zwei verschiedenen Arten von Selektoren:
1. ein HTML-Element wie z.B. h1, p oder ul
2. eine Klasse

Klasse werde ich nachher noch näher erklären. 
Eigenschaften sind z.B. Farbe (color) oder Schriftgröße (font-size) eines HTML-Elements. 
Der Wert ist dann z.B. der Farbname (z.B. green) oder die Größenangabe (z.B. 16px).

Wenn ich also die Überschrift h1 in meiner Website grün einfärben möchte, dann muss ich folgende CSS-Anweisung angeben:

```css
h1 {
	color: green;
}
```

h1 ist der Selektor, color ist die Eigenschaft und green der Wert.

## Wie kommt das CSS in meine HTML-Datei?
### Externe Stylesheets

Es gibt verschiedene Möglichkeiten eine CSS-Datei in ein HTML-Dokument einzubinden. Die beste und professionellste ist eine eigene externe CSS-Datei.

Dazu legst du im Editor eine neue Datei an und speicherst diese unter **styles.css** im gleichen Verzeichnis wie deine HTML-Datei.

Nun wollen wir einmal versuchen die Überschrift h1 grün einzufärben.

Tippe dazu folgendes in die **styles.css** ein:

```css
h1 {
  color: red;
}
```

Abspeichern nicht vergessen.

Dann müssen wir die CSS-Datei noch in die HTML-Datei einfügen. Dazu tippst du folgende Zeile in deine HTML-Datei:

```html
<head>
  <link rel=“stylesheet“ type=“text/css“ href=“styles.css“ />
...  
</head>
```

Speichern nicht vergessen! Wenn du alles richtig gemacht hast und du dir die Seite im Browser ansiehst, sollte die Überschrift jetzt grün sein.

## Verschiedene styles
Es gibt natürlich viele verschiedene Eigenschaften, die ein Text haben kann. Wir können z.B. auch die Textgröße ändern. Du hast z.B. das Element (Tag) `<p>` für Absätze in deiner HTML-Datei. Wir wollen die Schrift in diesen Absätzen etwas größer machen.

Dazu brauchen wir die CSS-Anweisung **font-size**.

Gib folgende Anweisung in deine CSS-Datei ein:

```css
p {
  font-size: 16px;
}
```

Der Wert **16px** ist die Größenangabe für die Schrift und px ist dabei die Maßeinheit. Speicher deine CSS-Datei ab und schau dir die HTML-Datei im Browser an.

### Weitere Textformate
Wie wäre es mit einer anderen Schriftstärke. Diese können wir mit **font-weight** festlegen.
Ergänze folgendes in deiner CSS-Datei:

```css
p {
  font-size: 16px;
  font-weight: bold;
}
```

Abspeichern und im Browser die Webseite anschauen. Nun müssten alle Absätze fett erscheinen. Hier eine kleine Liste von möglichen Textformaten:

* font-weigth: Schriftstärke ändern (siehe oben)
  Mögliche Werte: lighter, light, normal, bold, bolder
* font-family: Schriftart ändern
  Mögliche Werte: alle Schriften, die auf dem Computer installiert sind
```css
p{
font-family: Verdana, arial;
}
```
* font-style: Schriftstil ändern
  mögliche Werte: italic, oblique, normal
```css
p {
font-style: italic;
}
```
* text-decoration: einen Text dekorieren, z.B unterstreichen
    mögliche Werte: underline, overline, line-through, none
```css
p {
text-decoration: underline;
}
```

Damit lässt sich schon einiges gestalten. Probier es einfach mal aus und tippe verschiedene Textformate in deine CSS-Datei ein. Schau dir die Ergebnisse im Browser an.

## Klassen bilden
Mit den Tags und den CSS-Angaben kannst du in deiner Webseite schon ziemlich viel verändern und formatieren.
Aber wenn du eine CSS-Anweisung z.B für den Absatz p einfügst, dann hast du sicherlich bemerkt, dass dann alle Absätze p diese Formatierungen übernehmen. Aber wie kann man nur einen speziellen Absatz z.B. fett gestalten oder mit einer anderen Farbe einfärben?

Dafür brauchen wir Klassen. Mit Klasse ist keine Schulklasse gemeint, sondern mit einer CSS-Klasse kannst du eine Formatierung, die du einmal erstellt hast für mehrere Tags verwenden, indem du in diesem Tag diese Klasse angibst. Der englische Begriff dafür ist **class**.

Ein Klassennamen wird gebildet, indem man sich einen passenden Namen für die Klasse ausdenkt und diesen mit einem Punkt davor in der CSS-Datei angibt. In der HTML-Datei müssen wir dann die Klasse im jeweiligen Tag einfügen.

In deiner HTML-Datei färben wir so nun die Schrift in einem Absatz grün. Folgendes musst du dazu ergänzen:

```html
<p class=“gruen“>
 Hier steht dein Text, der grün werden soll.

 Es kann auch eine Leerzeile drin sein.
</p>
```

In der CSS-Datei brauchen wir nun die entsprechende Klassen-Definition:

```css
.gruen {
 color: green;
}
```

Schau dir das Ergebnis im Browser an. Natürlich speichern nicht vergessen.

Mit den Klassen hast du also die Möglichkeit in jedem gewünschten Tag die Schrift oder Farbe oder beides zu verändern. Du musst nur die Klasse in dem Tag angeben.

##Verschachtelte Selektoren

Ein Selektor kann auch aus mehreren einzelnen Selektoren bestehen. Z.B. kann ich aus mehreren Absatzes p nur bestimmte Elemente selektieren, indem ich die Selektoren verschachtelt angebe.

Ein Beispiel: 
Ich habe zwei Absätze p und möchte aber nur die Listenpunkte vom zweiten Absatz p mit der Klasse gruen auswählen.

Hier der HTML-Code:

```html
<p>
 	Hier steht ein toller Text und eine schöne Liste:
 	<ul>
		<li>Listenpunkt1</li>
		<li>Listenpunkt2</li>
	</ul>
</p>
<p class=“gruen“>
 	Hier steht ein toller grüner Text und eine schöne Liste:
 	<ul>
		<li>Listenpunkt1</li>
		<li>Listenpunkt2</li>
	</ul>
</p>
```

Die CSS-Anweisung lautet für die Listenpunkte im zweiten Absatz nun so:

```css
p.gruen ul li {
 color: red;
}
``` 
Somit werden die Listenpunkte im zweiten Absatz mit der Klasse gruen in der Farbe Rot ausgegeben. Probier es doch einfach aus und tippe den Code in deine HTML- und CSS-Datei. 

## Noch mehr CSS-Angaben
Es gibt natürlich noch ganz viele CSS-Eigenschaften, die man in seiner Webseite verwenden kann. Z.B. möchtest du vielleicht die Abstände zwischen zwei Absätzen ändern oder den Text einrücken.

Dafür gibt es folgende CSS-Anweisungen:
* margin: Außenabstände
* padding: Innenabstände

Man kann den Abstand rundherum mit dem gleichen Wert ändern oder jede Seite extra (also oben, rechts, unten, links):
* margin-top, margin-right, margin-bottom, margin-left
* padding-top, padding-right, padding-bottom, padding-left

Ergänze folgende Anweisung in deiner CSS-Datei:

```css
.gruen {
color: green;
padding-left: 20px;
margin-top: 50px;
}
```

Abspeichern und dann schau dir das Ergebnis im Browser an.

Wenn alles richtig ist, dann ist der Absatz mit grüner Schrift links weiter eingerückt und hat oben einen größeren Abstand.
In deiner Webseite befinden sich noch andere Tags, wie z.B. die Liste `<ul>`. Diese lässt sich auch einrücken, damit deutlich wird, dass es sich um eine Liste handelt.

Ergänze folgende CSS-Angabe in deiner CSS-Datei:

```css
ul {
padding-left: 30px;
}
```

Wenn du abspeicherst und die HTML-Seite im Browser ansiehst, kannst du sehen, dass die Liste nun links weiter eingerückt ist.
Mit diesem Grundwissen kannst du nun schon einiges schöner gestalten in deiner Webseite.

Probier es einfach aus. Bei Fragen kannst du dich jederzeit an die Mentoren wenden.
Wie wäre es mit einer eigenen kleinen Webseite?
Viel Spaß dabei!
