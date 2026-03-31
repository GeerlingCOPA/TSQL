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
- dbo.cop_sp_modifyextendedproperty nur positionsbasiert aufrufen
- Keine benannten Parameter wie @_value oder @_level1name beim Aufruf von dbo.cop_sp_modifyextendedproperty verwenden
- NULL-Werte beim positionsbasierten Aufruf an der korrekten Parameterposition explizit mitgeben
- Für längere Beschreibungstexte VARCHAR(4000)-Variablen verwenden
- Längere Beschreibungstexte nicht als mehrzeilige Literale direkt im EXEC übergeben

## Antworten und Arbeitsweise
- Antworten allgemein und dokumentationstauglich formulieren
- Keine direkte persönliche Anrede verwenden
- Excel-Ausgaben für Copy und Paste als echte tab-getrennte Blöcke liefern
- Keine Markdown-Tabellen verwenden, wenn die Ausgabe nach Excel kopiert werden soll

## Merksatz
- T-SQL immer im Hausstil gemäß dieser Datei formulieren