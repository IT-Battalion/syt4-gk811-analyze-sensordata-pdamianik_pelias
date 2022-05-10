## Research
- Welche Probleme können bei der Verwendung von Sensoren auftreten?

  > 

- Wie sind externe Sensoren anzusprechen? Welche verbreitete Protokolle gibt es dabei?

  > | Name     | Description                                 | Function                                                     |
  > | -------- | ------------------------------------------- | ------------------------------------------------------------ |
  > | **I2C**  | Inter-Integrated Circuit                    | Half duplex, serial data transmission used for short-distance between boards, modules and peripherals. Uses 2 pins. |
  > | **SPI**  | Serial Peripheral Interface bus             | Full-duplex, serial data transmission used for short-distance between devices. Uses 4 pins. |
  > | **UART** | Universal Asynchronous Receiver-Transmitter | Asynchronous, serial data transmission between devices. Uses 2 pins. |
  >
  > [1]
  >
  > Sensoren steckt man an die dafür vorgsehenen Pins an. Diese sind im normalfall beschriftet, ansonsten kann man die Pins auch online nachschalgen. Diese Pins kann man dann mit den jeweiligen Protkoll ansprechen und Anweisungen an den Sensor senden.

- Wie können Daten aggregiert werden? Welche Anforderungen müssen dabei beachtet werden?

  > Mit "Daten aggregieren" werden  Fallgruppen im aktiven Dataset zu einzelnen Fällen kombiniert; hierbei  wird eine neue, aggregierte Datei angelegt oder es werden neue Variablen im aktiven Dataset angelegt, die aggregrierte Daten enthalten. Die  Fälle werden nach *null* oder mehreren Werten von  Breakvariablen (Gruppierungsvariablen) aggregiert. Wenn keine  Breakvariablen angegeben sind, ist das gesamte Dataset eine einzige  Breakgruppe.
  >
  > -  Wenn  Sie eine neue, aggregierte Datendatei anlegen, enthält diese neue Datei  je einen Fall für jede Gruppe, die in den Breakvariablen definiert sind. Liegt beispielsweise eine Breakvariable mit zwei Werten vor, enthält  die neue Datendatei nur zwei Fälle.  Wenn keine Breakvariable angegeben  ist, enthält die neue Datendatei nur einen Fall. 
  > - Wenn Sie Aggregationsvariablen in das  aktive Dataset aufnehmen, wird die Datendatei selbst nicht aggregiert.  Jeder Fall mit denselben Werten für die Breakvariable(n) erhält  dieselben Werte für die neuen Aggregationsvariablen. Wenn beispielsweise nur eine Breakvariable *geschl* vorliegt, erhalten  alle männlichen Personen denselben Wert für eine neue  Aggregationsvariable, die das Durchschnittsalter erfasst. Wenn keine  Breakvariable angegeben ist, erhalten alle Fälle denselben Wert für eine neue Aggregationsvariable, die das Durchschnittsalter repräsentiert. 
  >
  >  **Breakvariable(n).** Die Fälle  werden auf der Basis der Breakvariablen gruppiert. Jede eindeutige  Kombination von Breakvariablenwerten definiert eine Gruppe. Wenn Sie  eine neue, aggregierte Datendatei erstellen, werden alle Breakvariablen  in der neuen Datei unter dem bisherigen Namen und mit den vorhandenen  Informationen aus dem Datenwörterbuch gespeichert. Die Breakvariablen  können, wenn angegeben, numerische Variablen oder Zeichenfolgevariablen  sein.
  >
  >  **Aggregierte Variablen.**  Quellenvariablen werden in Verbindung mit Aggregationsfunktionen zum  Erzeugen der neuen Aggregationsvariablen herangezogen. Der Name der  Aggregationsvariablen wird von einer optionalen Variablenbeschriftung,  dem Namen der Aggregationsfunktion und der Quellenvariablen in Klammern  gefolgt. 
  >
  > Sie können die vorgegebenen Namen für die  Aggregationsvariablen mit neuen Variablennamen überschreiben,  aussagekräftige Variablenbeschriftungen verwenden und die Funktionen zum Berechnen der aggregierten Datenwerte ändern. Sie können auch eine  Variable anlegen, welche die Anzahl der Fälle in jeder Breakgruppe  enthält.
  >
  >  So aggregieren Sie eine Datendatei:
  >
  > 1. Wählen Sie in den Menüs Folgendes aus:
  >
  >     Daten > Aggregieren... 
  >
  > 2. Wählen Sie optional Breakvariablen aus,  die definieren, wie die Fälle zum Erzeugen der aggregierten Daten  gruppiert werden. Wenn keine Breakvariablen angegeben sind, ist das  gesamte Dataset eine einzige Breakgruppe.
  >
  > 3. Wählen Sie mindestens eine Aggregationsvariable aus.
  >
  > 4. Wählen Sie für jede Aggregationsvariable eine Aggregationsfunktion aus.
  >
  > Zusätzlich können Sie die vorgegebenen Namen für die  Aggregationsvariablen mit neuen Variablennamen überschreiben,  aussagekräftige Variablenbeschriftungen verwenden und eine Variable  anlegen, welche die Anzahl von Fällen in jeder Breakgruppe enthält.
  >
  >   Speichern von aggregierten Ergebnissen 
  >
  > Sie können wahlweise Aggregationsvariablen in das aktive Dataset aufnehmen oder eine neue, aggregierte Datendatei erzeugen.
  >
  > -  Aggregierte Variablen zum aktiven Dataset hinzufügen. Neue Variablen, die auf Aggregierungsfunktionen beruhen, werden zum aktiven  Dataset hinzugefügt. Die Datendatei selbst wird nicht aggregiert. Jeder Fall mit denselben Werten für die Breakvariable(n) erhält  dieselben Werte für die neuen Aggregationsvariablen. 
  > -  Neues Dataset erstellen, das nur die aggregierten Variablen enthält. Speichert die aggregierten Daten in einem neuen Dataset in der aktuellen Sitzung. Das Dataset enthält die Breakvariablen, die die aggregierten Fälle  bestimmen, und alle aggregierten Variablen, die durch  Aggregationsfunktionen definiert werden. Das aktive Dataset bleibt davon unberührt. 
  > -  Neue Datendatei erstellen, die nur die aggregierten Variablen enthält. Speichert die aggregierten Daten in einer externen Datendatei. Die Datei enthält  die Breakvariablen, die die aggregierten Fälle bestimmen und alle  aggregierten Variablen, die durch Aggregationsfunktionen definiert  werden. Das aktive Dataset bleibt davon unberührt. 
  >
  >   Sortieroptionen für umfangreiche Datendateien 
  >
  > Bei äußerst umfangreichen Datendateien empfiehlt es sich, die Dateien vor der Aggregation zu sortieren.
  >
  >  Die Datei ist bereits anhand einer oder mehrerer Breakvariablen sortiert. Wenn die Daten bereits nach den Werten der Breakvariablen sortiert wurden,  sorgt diese Option für einen schnelleren Ablauf der Prozedur und  geringeren Speicherplatzbedarf. Diese Option sollte mit Bedacht  verwendet werden. 
  >
  > - Die  Daten müssen nach den Werten der Breakvariablen sortiert werden, und  zwar in derselben Reihenfolge wie die Breakvariablen, die für die  Funktion "Daten aggregieren" angegeben wurden. 
  > - Wenn Sie Variablen in das aktive Dataset  aufnehmen, wählen Sie diese Option nur dann aus, wenn die Daten anhand  der Werte der Breakvariablen in aufsteigender Reihenfolge sortiert sind.
  >
  >  Datei vor Aggregation sortieren. In sehr seltenen Fällen kann es bei großen Datendateien nötig sein, die  Datendatei vor dem Aggregieren nach den Werten der Breakvariablen zu  sortieren. Diese Option ist nur dann angeraten, wenn Speicher- bzw.  Leistungsprobleme auftreten. 
  >
  > [2]

- Wie können zeitabhängige Messdaten leicht gespeichert und verarbeitet werden?

  > - Identifizieren Sie existierende Datenquellen in Ihrem Unternehmen. Nicht immer ist zusätzliche Sensorik nötig.
  >
  > - Verwenden Sie Aufzeichnungsintervalle, die genau zu Ihrem Szenario  passen. Unnötig kurze Intervalle erzeugen immense Datenmengen.
  >
  > - Wählen Sie das passende Datenbanksystem für Ihren Anwendungsfall. TimescaleDB ist für Zeitreihendaten eine gute Wahl.
  >
  > - Dimensionieren und konfigurieren Sie den Datenbankserver so, dass  benötigte Tabellenindizes im Arbeitsspeicher gehalten werden können.
  >
  > - Behalten Sie Ausführungszeiten von Datenbankabfragen im Auge. Können Indizes nicht mehr im RAM gehalten werden, sinkt die Performance  drastisch.
  >
  > - Nutzen Sie optimierte Sonderfunktionen Ihres Datenbanksystems.
  >
  > - Binden Sie erstellte Visualisierungen in schon vorhandene Dashboards und Webanwendungen im Unternehmen ein, um das daraus ableitbare Wissen  breit nutzen zu können.
  >
  > - Behalten Sie den wachsenden Datenbestand im Auge, um beteiligte Systeme frühzeitig skalieren zu können.
  >
  > - Hinterfragen Sie die angenommenen Parameter zu gegebener Zeit. Gibt  es Haupt- und Nebenzeiten mit unterschiedlicher Nutzung der Anlagen?  Variable Intervalle für die Datenablage können das Speichervolumen stark reduzieren.
  >
  > - Erhöhen Sie – wenn möglich – nur die Speicherintervalle, nicht die  Abfrageintervalle der Sensoren. So können Sie noch mit der gleichen  Geschwindigkeit auf Änderungen reagieren.
  >
  >   [3]

- Welche Möglichkeiten gibt es Daten zu vergleichen und diese zur Steuerung einzusetzen?

  > 

- Was muss beim Einsatz eines SBCs oder Mikrocontrollers zur fortwährenden Aufnahme von Messdaten beachtet werden?

  > 

## Quellen

[1] "Raspberry Pi  I2C  /  SPI  /  UART  Communications"; mbtechworks; https://www.mbtechworks.com/hardware/raspberry-pi-UART-SPI-I2C.html, zuletzt beuscht am 10.06.2022

[2] "Daten aggregieren"; IBM; https://www.ibm.com/docs/de/spss-statistics/25.0.0?topic=transformations-aggregate-data, zuletzt besucht am 10.06.2022

[3] "Performante Speicherung und Visualisierung von Sensordaten"; Betrieb-Machen; https://betrieb-machen.de/sensordaten-performant-speichern-und-visualisieren/; zuletzt besucht am 10.06.2022





