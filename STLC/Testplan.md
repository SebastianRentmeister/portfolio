# Testplan # 
https://grocerymate.masterschool.com/
### 1. Produktanalyse ###
- Zielsetzung:
Das Hauptziel des Produkts ist die Erweiterung des GroceryMate Webshops durch neue Funktionen für Kunden. 
Gleichzeitig soll sichergestellt werden, dass bisherige Funktionen weiterhin stabil arbeiten und die Benutzerfreundlichkeit erhalten bleibt. 

- Zielgruppe:
Die Webseite richtet sich an Nutzer, die Lebensmittel und Haushaltsprodukte online bestellen möchten. 

####  Hardware- und Software-Spezifikationen: ####

- Hardwareanforderungen: Laptop
Mindestanforderungen: Keine spezifischen Mindestanforderungen definiert
- Softwareanforderungen:
Betriebssysteme: Windows
Browser: Chrome
Abhängigkeiten: Datenbanken, Zahlungsschnittstellen, Versanddienstleister, Backend-System des Webshops

#### Testlogistik & Verantwortlichkeiten: ####

Testplanung & Testmanagement: Sebastian Rentmeister
Testfalldesign & Testdurchführung (Funktion, Regression, Usability): Sebastian Rentmeister

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

#### Aussetzungskriterien (Suspension Criteria) ####

- Die Webseite ist nicht erreichbar oder lädt nicht (z. B. durch Server-Ausfall oder abgelaufenes Sicherheitszertifikat).
-  Die Produktdatenbank kann nicht abgerufen werden oder Test-Nutzerkonten funktionieren nicht, wodurch der Warenkorb nicht getestet werden kann. 

#### Abnahmekriterien (Exit Criteria) ####

- Versandkosten müssen richtig berechnet werden 
- Altersprüfung muss Minderjährige blockieren 
- Bewertungen werden korrekt gespeichert 
- 100% der Testfälle werden durchgeführt 

### 5. Ressourcenplanung: ###

- Personelle Ressourcen: Sebastian Rentmeister (QA Engineer / Tester)
- Hardware: Laptop (Windows)
- Software: Chrome,
- Infrastruktur: www.grocerymate.masterschool.com 

### 6. Testumgebung planen ###

- Testgeräte: 1x Laptop 
- Umgebungen: Der Webshop Grocery Mate, bereitgestellt von der Masterschool. 

### 7. Zeitplan und Aufwandsschätzung ###


| Aktivität | Startdatum | Enddatum | Umgebung | Verantwortlich | Geplanter Aufwand |
| --- | --- | --- | --- | --- |-------------------|
| Anforderungsanalyse | 06.07.2026 | 12.07.2026 | TEST | Sebastian Rentmeister | 5 Stunden         |
| Testplanung & Design | 13.07.2026 **| 19.07.2026 | TEST | Sebastian Rentmeister | 5 Stunden         |
| Umgebung & Durchführung | 20.07.2026 | 26.07.2026 | TEST | Sebastian Rentmeister | 8 Stunden         |


### 8. Testartefakte (Test-Deliverables): ###

#### Folgende Dokumente und Werkzeuge werden im Rahmen des Testprozesses erstellt und bereitgestellt: ####

- Testplandokument
- Testfälle und Testskripte
- Testdaten
- Testberichte
- Fehlerberichte (Defect Reports)