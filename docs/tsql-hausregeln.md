# T-SQL Hausregeln

## Gültigkeit
- SQL Server 2016

## Syntax und Formatierung
- Keine Semikolons verwenden
- Keine Kommentare mit -- verwenden
- Kommentare nur als Blockkommentare mit /* ... */
- Batches ausschließlich mit GO trennen
- Funktionsaufrufe positionsbasiert formulieren

## Benennung
- Programmteile beginnen in der Regel mit COP_

## Dokumentation
- Dokumentation über MS_Description pflegen
- Extended Properties über dbo.cop_sp_modifyextendedproperty setzen
- Für @_value keine NVARCHAR(MAX)-Werte verwenden
- Beschreibungstexte für Extended Properties nicht als mehrzeilige Literale direkt im EXEC übergeben
- Längere Beschreibungstexte zuerst in einer NVARCHAR(4000)-Variable aufbauen und dann an @_value übergeben

## Antworten und Arbeitsweise
- Antworten allgemein und dokumentationstauglich formulieren
- Keine direkte persönliche Anrede verwenden
- Excel-Ausgaben für Copy und Paste als echte tab-getrennte Blöcke liefern
- Keine Markdown-Tabellen verwenden, wenn die Ausgabe nach Excel kopiert werden soll

## Merksatz
- T-SQL immer im Hausstil gemäß dieser Datei formulieren