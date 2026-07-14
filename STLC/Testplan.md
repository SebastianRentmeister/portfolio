# Testplan # 
https://grocerymate.masterschool.com/
### 1. Produktanalyse ###
- Zielsetzung:
Das Hauptziel des Produkts ist die Erweiterung des GroceryMate Webshops durch neue Funktionen für Kunden. 
Gleichzeitig soll sichergestellt werden, dass bisherige Funktionen weiterhin stabil arbeiten und die Benutzerfreundlichkeit erhalten bleibt. 

- Zielgruppe:
Die Webseite richtet sich an Nutzer, die Lebensmittel und Haushaltsprodukte online bestellen möchten. 

####  Hardware- und Software-Spezifikationen: ####

- Hardwareanforderungen:
PCs und Laptops, Smartphones, Tablets  
Mindestanforderungen: Keine spezifischen Mindestanforderungen definiert
- Softwareanforderungen:
Betriebssysteme: Windows, macOS, Android, iOS
Browser: Chrome, Firefox, Safari, Edge
Abhängigkeiten: Datenbanken, Zahlungsschnittstellen, Versanddienstleister, Backend-System des Webshops

#### Funktionalitäten: ####

- Produktsuche
- Registrierung/Login/Logout 
- Produkte als Favoriten markieren 
- Gekaufte Produkte über Feedbackfunktion bewerten 
- Produkte in den Warenkorb legen
- Altersverifizierung für alkoholische Produkte  
- Bestellvorgang 

### 2. Teststrategie entwerfen: ###
Testumfang:

Im Umfang enthalten: 

- Altersverifikation für alkoholische Produkte
- Bewertungssystem für Produkte
- Änderungen der Versandkosten (versandkostenfrei oder kostenpflichtig)

Außerhalb des Umfangs:

- Backend-System des Webshops
- Zahlungsschnittstellen
- Datenbanken 

Testarten:

- Funktionstests
- Regressionstests
- Usability-Tests

Risiken und Probleme:

- **Entwicklungsverzögerungen**
    
→ Gegenmaßnahme: Zeitpuffer im Zeitplan einplanen
    
- **Fehlende Testdaten**
    
→ Gegenmaßnahme: Erstellen von Testdaten (Mock-Daten)
(Test Nutzerkonten mit Geburtsdatum vor und nach 2008, Warenkörbe unter und über dem Grenzwert)
    
- **Ressourcenengpässe**
    
→ Gegenmaßnahme: Ersatzpersonen identifizieren und einplanen

### 3. Testziele definieren ###

Funktionalität: 
- Sicherstellen, dass die Altersprüfung Minderjährige blockiert
- Ab dem Grenzwert sollen Versandkosten 0€ betragen 
- Bewertungen werden korrekt gespeichert

Benutzeroberfläche (GUI): 
- Überprüfung, ob die neuen Eingabefelder (Geburtsdatum, Bewertungssterne, Feedback Eingabefeld) auf Smartphones und PCs fehlerfrei angezeigt werden.

Benutzbarkeit (Usability): 
- Testen, ob der Kunde ohne Anleitung versteht, wie er eine Bewertung abgibt und warum er sein Alter angeben muss.

#### Erwartete Ergebnisse: ####

- Minderjährige Nutzer bekommen eine Hinweismeldung, dass sie nicht zum Kauf berechtigt sind. 
- Nutzer über 18 Jahre können alkoholische Produkte bestellen.
- Ab einem festgelegten Grenzwert ist die Bestellung versandkostenfrei, eine Bestellung die unter dem Grenzwert liegt wird mit den jeweiligen Versandkosten berechnet.
- Das Feedback ist nach dem Absenden für andere Nutzer ersichtlich und wird gespeichert.
- Wenn der Nutzer kein Feedback hinterlässt und das Eingabefeld leer bleibt, wird darauf mit einer Meldung hingewiesen und die Bewertung wird nicht gesendet.

### 4. Testkriterien definieren ###
