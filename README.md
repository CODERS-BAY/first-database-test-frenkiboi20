# DB-Test
## Aufgabe 1
Stelle Entitäten mittels Chen-Notation und Min,Max Notation dar.
Wähle ein sinnvolles Beispiel!
In einer Filiale arbeiten 1 bis n Mitarbeiter. Ein Mitarbeiter arbeitet in einer Filiale.
Mitarbeiter (1,1) -- arbeitet -- (1,n) Filiale(n)
Mitarbeiter n -- arbeitet in -- 1 Filiale
(siehe Grafik: Aufgabe1.png)

## Aufgabe 2
Kann eine Beziehung Attribute haben?
Ja, kann sie.
Wenn ja, wie stelle ich es im ERD dar?
In einer Ellipse über der Beziehung

## Aufgabe 3
Welche Codd'schen Anforderungen gibt es (Nenne mindestens 5)
Integration, Operation, Synchronisation, Benutzersichten, Integritätssicherung, Zugriffskontrolle, Transaktion, Datensicherung, Katalog

## Aufgabe 4
Nenne den Unterschied zwischen Konzeptuellen und Logischem Schema
Konzeptuelles Schema: ist das Entity-Relationship-Modell
Logisches Schema: wird aus den Anforderungen heraus entwickelt und bildet die Fachlichkeit ab.

## Aufgabe 5
Welche 3 Bestandteile gibt es im Entity Relationship Model
Entity, Relationship, Attribute

## Aufgabe 6
Welche Datentypen gibt es in MySQL? (Nenne mindestens 5)
INTEGER, BIGINT, SMALLINT, FLOAT, DOUBLE, NUMERIC, DECIMAL, NUMBER, CHARACTER

## Aufgabe 7
Welche Arten von Schlüsseln gibt es und welche Eigenschaften besitzen diese?
Primärschlüssel: ist eindeutig, künstlich und zusammengesetzt
Fremdschlüssel: dieser darf nur Werte annehmen die der Primärschlüssel in der Tabelle hat

## Aufgabe 8
Welche Arten von Beziehungen gibt es? Zeichne für jede ein Beispiel auf
1:N - Beziehung: 1 Kunde ordert n Bestellungen - n Bestellungen werden von 1 Kunden geordert
1:1 - Beziehung: Zu 1 Fahrzeug gehört 1 Kennzeichen - 1 Kennzeichen gehört zu einem Fahrzeug 
M:N - Beziehung: n Magazine enthalten m Artikel - m Artikel werden von n Magazinen beinhaltet
(siehe Grafik: Aufgabe8.png)

## Aufgabe 9
Was bedeutet der Begriff Kardinalität und welche Kardinalitäten gibt es?
Die Kardinalität bestimmt verschiedene Ausmaße zu einer Datenbanktabelle

## Aufgabe 10
Was bedeutet der Begriff Datenintegrität und worin unterscheidet sich Integrität und referentielle Integrität?
Datenintegrität bezieht sich auf die Korrektheit, Vollständigkeit und Konsistenz von Daten

## Aufgabe 11
Erkläre die 3 Normalformen
1NF: Alle Elemente müssen atomar sein. Das heißt die Datensätze müssen auf die kleinste Menge an relevante Daten reduziert werden.
2NF: Redundanzen beseitigen
3NF: Balance aus Performance, Flexibilität und Redundanzen

## Aufgabe 12
Erkläre den Unterschied zwischen starken und Schwachen Entitäten und erstelle ein Beispiel.
Die Existenz einer starken Entität ist nicht abhängig von der Existenz einer anderen Entität. Ausserdem hat sie einen Primärschlüssel.
Eine schwache Entität ist immer von ihrer Eigentümerentität abhängig.

## Aufgabe 13
Welche Grundregeln gibt es im Relationenmodell? (Nenne mindestens 4)
Reihenfolge der Zeilen ist bedeutungslos
Reihenfolge der Spalten ist bedeutungslos da sie eindeutige Attributnamen haben
Jeder Datenwert ist ein atomares Element
Alle für Benutzer relevanten Informationen sind ausschließlich durch Datenwerte ausgedrückt

## Aufgabe 14
Wie löst man eine M:N Beziehung auf? Erstelle ein Beispiel
Mit einer assoziativen Tabelle
m:n wird zu m:1 und 1:n
(siehe Grafik: Aufgabe14.png)

## Aufgabe 15
Ein Handelsbetrieb verkauft ein Sortiment von Artikeln, die er von verschiedenen Herstellern bezieht. Der Handelsbetrieb hat einen bestimmten Kundenkreis, der regelmäßig Bestellungen aufgibt. Eine Bestellung kann mehrere Artikel umfassen. Ein Artikel kann von mehreren Lieferanten bezogen werden und ein Lieferant liefert natürlich meist mehr als einen Artikel. Erstelle ein ERD und ein Relationenmodell, welches der 3. Normalform entspricht.
(siehe Grafik: Aufgabe15.png)

## Aufgabe 16
Welche Anomalien kennst du und was beschreiben sie?
Insert-, Update- und Delete-Anomalien
Insertanomalie: Entweder werden Daten nicht übernommen, oder unvollständige Eingabe von Daten führt zur Inkonsistenz
Updateanomalie: Bei einer Änderung im Datensatz werde gleiche Attribute nicht automatisch geändert
Deleteanomalie: Wenn man Daten löschen will und damit indirekt  aufgrund eines fehlerhaften Designs andere zusammenhängende Informationen mitlöscht

## Aufgabe 17
Modellieren Sie den angeführten Realitätsausschnitt einer Fluggesellschaft mit Hilfe eines Entity Relationship- Diagramms. Treffen Sie, falls notwendig, sinnvolle Annahmen und dokumentieren Sie diese nachvollziehbar in Ihrer Lösung. Der zu betrachtende Realitätsausschnitt der Fluggesellschaft umfasst folgenden
Sachverhalt:
Flughäfen haben ein Kürzel (= Schlüssel) und gehören zu einer Stadt (z.B. „FRA“ für Frankfurt, „FCO“ für Roma Fiumicino).
Flüge haben eine Flugnummer (z.B. „LH 306“), führen von einem Flughafen zu einem anderen, mit jeweils einer festen Abflugs- und Ankunftszeit (z.B. ab Frankfurt um 07:30 nach Roma Fiumicino mit Ankunft um 09:15).
Jeder Flugzeugtyp hat einen Namen (z.B. „747-400“) und eine Sitzanzahl (z.B. 430 Sitze).
Piloten haben einen Namen (z.B. „Meier“), ein Geburtsdatum (z.B. „1.1.1960“) und eine Berechtigung, bestimmte Flugzeugtypen zu fliegen (z.B. „747-400“ und „A310“).
Jedes einzelne Flugzeug ist von einem bestimmten Flugzeugtyp (z.B. „747-400“) und hat einen Namen (z.B. „Mozart“).
Bei einem Flug-Einsatz wird ein Flug (z.B. „LH 306“) an einem bestimmten Datum (z.B. „6.2.2011“) von einem bestimmten Piloten (z.B. „Meier“) mit einem bestimmten Flugzeug (z.B. „Mozart“) geflogen.
Bilden Sie das konzeptuelle Schema in ein relationales Schema ab. Das relationale Schema soll der 3. Normalform genügen
