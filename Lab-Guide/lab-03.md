## Inhalt
- Einführung
- Dataflow Gen2
  - Aufgabe 1: Dataflow Gen2 erstellen
  - Aufgabe 3: Die Abfrage für den Ordner „Base ADLS Gen2“ erstellen
  - Aufgabe 2: Verbindung zu ADLS Gen2 herstellen
  - Aufgabe 4: Abfrage „Cities“ erstellen
  - Aufgabe 5: Abfrage „Countries“ erstellen
  - Aufgabe 6: States mit Kopieren – Option 1 erstellen
  - Aufgabe 7: Abfrage „Geo“ mit Kopieren erstellen – Option 2
  - Aufgabe 8: Datenziel für die Abfrage „Geo“ konfigurieren
  - Aufgabe 9: Dataflow veröffentlichen
  - Aufgabe 10: Dataflow umbenennen
  - Aufgabe 11: Verbleibende Abfragen im Dataflow erstellen
  - Aufgabe 12: Datenziel für verbleibende Abfragen konfigurieren
- Referenzen

## Einführung
In unserem Szenario stammen die Verkaufsdaten aus dem ERP-System und werden in einer ADLS Gen2 gespeichert. Jeden Tag um 12 Uhr mittags werden die Daten aktualisiert. Wir müssen diese Daten transformieren, in Lakehouse erfassen und in unserem Modell verwenden.

Es gibt mehrere Möglichkeiten, diese Daten zu erfassen.



- **Verknüpfungen**: Hiermit können keine Daten transformiert werden.
- **Notebooks**: Dafür müssen wir Code schreiben. Es handelt sich um einen entwicklerfreundlichen Ansatz.
- **Dataflow** Gen2: Sie sind wahrscheinlich mit Power Query oder Dataflow Gen1 vertraut. Dataflow Gen2 ist, wie der Name schon sagt, die neuere Version von Dataflow. Es bietet alle Funktionen von Power Query/Dataflow Gen1 und ermöglicht zusätzlich die Transformation und Erfassung von Daten in mehreren Datenquellen. Wir werden dies in den nächsten
Übungen vorstellen.
- **Datenpipeline**: Dies ist ein Orchestrierungstool. Aktivitäten können orchestriert werden, um Daten zu extrahieren, zu transformieren und zu erfassen. Wir werden Data Pipeline verwenden, um Dataflow Gen2-Aktivitäten auszuführen, die wiederum Extraktion, Transformation und Aufnahme durchführen.

Wir beginnen mit Dataflow Gen2, um eine Verbindung zur Datenquelle und den notwendigen Transformationen herzustellen. Dann werden wir Dataflow Gen2 mit Data Pipeline
orchestrieren/ausführen. 

Inhalt dieser Übung:
  - So erstellen Sie Dataflow Gen2
  - So stellen Sie mithilfe von Dataflow Gen2 eine Verbindung zu ADLS Gen2 her und transformieren Daten
  - So erfassen Sie Daten in Lakehouse

## Dataflow Gen2
### Aufgabe 1: Dataflow Gen2 erstellen

1.	Navigieren wir zurück zum Fabric-Arbeitsbereich, den Sie in Übung 2, Aufgabe 9, erstellt haben.
2.	Wenn Sie nach der vorherigen Übung nicht zu einem anderen Bereich navigiert sind, befinden Sie sich im Lakehouse-Bildschirm. Wählen Sie unten links auf dem Bildschirm das Symbol Fabric- Funktionsbereichs-Auswahl aus.
3.	Wählen Sie im geöffneten Dialogfeld für den Fabric-Funktionsbereich Data Factory aus. Data Factory verfügt über Workloads, die zum Extrahieren, Transformieren und Erfassen von Daten erforderlich sind.
4.	Sie werden zur Data Factory-Startseite weitergeleitet. Wählen Sie unter „Neu“ die Option
Datenfluss Gen2 aus.

Sie werden zur **Dataflow-Seite** weitergeleitet. Dieser Bildschirm wird Ihnen bekannt vorkommen, da er Dataflow Gen1 oder Power Query ähnelt. Sie werden feststellen, dass die Optionen zum Herstellen einer Verbindung zu verschiedenen Datenquellen sowie die Möglichkeit zur Datentransformation verfügbar sind. Stellen wir eine Verbindung zur ADLS Gen2-Datenquelle her und führen einige Transformationen durch.

### Aufgabe 2: Verbindung zu ADLS Gen2 herstellen