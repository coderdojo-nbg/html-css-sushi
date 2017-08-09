# HTML-Elemente

Eine Auflistung der wichtigsten HTML-Elemente. Bis auf wenige Ausnahmen benötigen alle Elemente einen öffnenden und einen schließenden Teil, z.B. `<p> ... </p>`.
Ausnahmen (sog. "self-closing elements"): `<img>`, `<br>`, `<hr>`

## Basis HTML Grundstruktur

| Tag               | Beschreibung                                                                                               |
|:------------------|:-----------------------------------------------------------------------------------------------------------|
| `<!DOCTYPE html>` | Legt den HTML5-Dokumenttyp fest (streng genommen kein HTML-Element, sondern eine sog. Doctype-Deklaration) |
| `<html>`          | Wurzelelement eines HTML-Dokuments. Es ist das einzige Element auf der obersten Dokumentebene.             |
| `<head>`          | Enthält nicht unmittelbar sichtbare Informationen über das Dokument                                        |
| `<meta>`          | Meta-Angaben, z.B. die Zeichenkodierung des Dokuments                                                      |
| `<title>`         | Titel des Dokuments                                                                                        |
| `<link>`          | Vernknüpft eine externe Ressource mit dem Dokument (z.B. CSS-Stylesheet)                                   |
| `<script>`        | Bindet ein JavaScript ins Dokument ein (inline oder als externe Ressource)                                 |
| `<body>`          | Umschließt den sichtbaren Dokumentinhalt                                                                   |

## Bereiche HTML

| Tag         | Beschreibung                                                                                                |
|:------------|:------------------------------------------------------------------------------------------------------------|
| `<header>`  | Kopfbereich zu einem Abschnitt (kann mehrfach vorkommen)                                                            |
| `<nav>`     | Zentrale Navigation eines Dokuments (sollte nur einmal je Dokument verwendet werden)                        |
| `<main>`    | Hauptinhalt eines Dokuments (muss genau einmal vorkommen)                                                   |
| `<section>` | Abschnitt, der untergeordnete inhalte gruppiert und in der Regel eine Überschrift enthält.                  |
| `<article>` | In sich abgeschlossener, kontextunabhängig funktionierender Abschnitt, der untergeordnete Inhalte gruppiert |
| `<aside>`   | Ergänzender, aber positionsunabhängiger Zusatzinhalt                                                        |
| `<footer>`  | Fußbereich zu einem Abschnitt (kann mehrfach vorkommen)                                                     |
| `<div>`     | Semantisch neutraler Block-Container zum Gruppieren von Inhalten                                            |

## Textstrutkur HTML

| Tag               | Beschreibung                                                           |
|:------------------|:-----------------------------------------------------------------------|
| `<h1>`            | Hauptüberschrift (nur einmal pro Seite)                                |
| `<h2>` bis `<h6>` | Unterüberschriften — Verwendung in logischer und korrekter Hierarchie |
| `<p>`             | Absatz                                                                 |
| `<br>`            | Zeilenumbruch (benötigt kein schließendes Tag)                         |
| `<hr>`            | Trennlinie (benötigt kein schließendes Tag)                            |

## Textformatierung HTML

| Tag        | Beschreibung            |
|:-----------|:------------------------|
| `<strong>` | Texthervorhebung fett   |
| `<em>`     | Texthervorhebung kursiv |

## Links HTML

| Tag                               | Beschreibung                                                 |
|:----------------------------------|:-------------------------------------------------------------|
| `<a href="index.html">`           | Verknüpfung mit relativem URL (verweist auf dieselbe Domain) |
| `<a href="http://www.domain.de">` | Verknüpfung mit absolutem URL                     |

## Liste HTML

| Tag    | Beschreibung                                             |
|:-------|:---------------------------------------------------------|
| `<ul>` | Ungeordnete Liste (standardmäßig Listenpunkte)           |
| `<ol>` | Geordnete Liste (standardmäßig nummeriert)               |
| `<li>` | Einzelner Listenpunkt (Verwendung in `<ul>` oder `<ol>`) |

## Bilder

| Tag                                          | Beschreibung                             |
|:---------------------------------------------|:-----------------------------------------|
| `<img src="img.jpg" alt="Bildbeschreibung">` | Bild (benötigt keinen schließenden Teil) |
