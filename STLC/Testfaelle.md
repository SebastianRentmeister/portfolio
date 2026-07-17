## Altersverifikation ##

### Testfall 1: Erfolgreiche Altersverifikation 18. Geburtstag (Grenzwert)

| Schritt | Aktion                                                                              | Erwartetes Ergebnis | Ok/NOK | URL | Link to Issue |
| :--- |:------------------------------------------------------------------------------------| :--- | :--- | :--- | :--- |
| 1 | Klicke in der oberen blauen Navigationsleiste auf „SHOP“.                           | Das Pop-up „Age Verification“ erscheint mit der Aufforderung zur Geburtsdatums-Eingabe. | | | |
| 2 | Gib das Geburtsdatum für den exakten heutigen 18. Geburtstag ein (bsp. 15-07-2008). | Das Datum wird im Eingabefeld korrekt angezeigt. | | | |
| 3 | Klicke auf den Button „Confirm“.                                                    | Das Pop-up schließt sich, der Shop öffnet sich und alkoholische Produkte sind sichtbar und kaufbar. | | | |

### Testfall 2: Ungültiges Datumsformat ohne Trennzeichen (Negativtest)

| Schritt | Aktion | Erwartetes Ergebnis | Ok/NOK | URL | Link to Issue |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Klicke in der oberen blauen Navigationsleiste auf „SHOP“. | Das Pop-up „Age Verification“ erscheint mit dem Text: „You need to be +18 to see some products. Please enter your birth date:“. | | | |
| 2 | Gib ein Geburtsdatum ohne Bindestriche oder Punkte ein (z. B. 27031987). | Das System erkennt das falsche Format und eine Fehlermeldung (z. B. „Format wird nicht unterstützt“) wird angezeigt. | | | |
| 3 | Klicke auf den Button „Confirm“. | Der Zugriff auf den Shop bleibt gesperrt, bis ein gültiges Datumsformat eingegeben wird. | | | |

### Testfall 3: Absenden eines leeren Geburtsdatumsfeldes  ###

| Schritt | Aktion | Erwartetes Ergebnis | Ok/NOK | URL | Link to Issue |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Klicke in der oberen blauen Navigationsleiste auf „SHOP“. | Das Pop-up „Age Verification“ erscheint mit der Aufforderung zur Geburtsdatums-Eingabe. | | | |
| 2 | Lasse das Eingabefeld für das Geburtsdatum komplett leer. | Das Feld bleibt ohne Zeichen oder Zahlen. | | | |
| 3 | Klicke auf den Button „Confirm“. | Das System blockiert das Absenden. Das Pop-up schließt sich nicht und eine Fehlermeldung fordert zur Eingabe auf. | | | |

### Testfall 4: Sperrung eines minderjährigen Nutzers 

| Schritt | Aktion | Erwartetes Ergebnis | Ok/NOK | URL | Link to Issue |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Klicke in der oberen blauen Navigationsleiste auf „SHOP“. | Das Pop-up „Age Verification“ erscheint mit der Aufforderung zur Geburtsdatums-Eingabe. | | | |
| 2 | Gib ein Geburtsdatum ein, bei dem der Nutzer das 18. Lebensjahr noch nicht vollendet hat (z. B. das aktuelle Tagesdatum minus 15 Jahre). | Das Datum wird im Eingabefeld korrekt angezeigt. | | | |
| 3 | Klicke auf den Button „Confirm“. | Das System erkennt die Minderjährigkeit. Der Zugriff bleibt gesperrt und eine Hinweismeldung erscheint. | | | |

## Bewertungssystem ##

### Testfall 1 : Erfolgreiche Produktbewertung mit Sternen und Feedback ###

| Schritt | Aktion | Erwartetes Ergebnis | Ok/NOK | URL | Link to Issue |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Öffne die Detailseite eines bereits gekauften Produkts. | Die Produktseite lädt und der Bereich für das Feedback/die Bewertung ist sichtbar. | | | |
| 2 | Wähle eine Sternebewertung aus (z. B. 5 Sterne) und gib einen kurzen Text ein (z. B. „Super Produkt, schnelle Lieferung!“). | Die Sterne werden als ausgewählt markiert und der Text wird fehlerfrei im Eingabefeld angezeigt. | | | |
| 3 | Klicke auf den Button zum Absenden der Bewertung. | Die Bewertung wird erfolgreich gespeichert, das Eingabefeld schließt/leert sich und das Feedback ist für andere Nutzer sichtbar. | | | |

### Testfall 2: Produktbewertung mit Text an der oberen Grenze  ###

| Schritt | Aktion | Erwartetes Ergebnis                                                                                      | Ok/NOK | URL | Link to Issue |
| :--- | :--- |:---------------------------------------------------------------------------------------------------------| :--- | :--- | :--- |
| 1 | Öffne die Detailseite eines bereits gekauften Produkts. | Die Produktseite lädt und der Bereich für das Feedback ist sichtbar.                                     | | | |
| 2 | Wähle eine Sternebewertung aus (z. B. 4 Sterne) und gib einen Text mit exakt 399 Zeichen in das Feedback-Feld ein. | Der Text wird ohne Kürzungen oder Fehler im Eingabefeld angezeigt.                                       | | | |
| 3 | Klicke auf den Button zum Absenden der Bewertung. | Die Bewertung wird erfolgreich gespeichert und der vollständige Text mit allen 399 Zeichen ist sichtbar. | | | |

### Testfall 3: Produktbewertung überschreitet maximale Zeichenanzahl ###

| Schritt | Aktion | Erwartetes Ergebnis                                                                                                                         | Ok/NOK | URL | Link to Issue |
| :--- | :--- |:--------------------------------------------------------------------------------------------------------------------------------------------| :--- | :--- | :--- |
| 1 | Öffne die Detailseite eines bereits gekauften Produkts. | Die Produktseite lädt und der Bereich für das Feedback/die Bewertung ist sichtbar.                                                          | | | |
| 2 | Wähle eine Sternebewertung aus und gib einen Text mit exakt 401 Zeichen in das Feedback-Feld ein. | Das System signalisiert entweder bereits beim Tippen den Fehler (z. B. durch Blockieren weiterer Zeichen) oder zeigt den Text an.           | | | |
| 3 | Klicke auf den Button zum Absenden der Bewertung. | Das Absenden wird blockiert. Eine Hinweismeldung erscheint, dass maximal 400 Zeichen erlaubt sind und die Bewertung wird nicht gespeichert. | | | |

### Testfall 4: Verwendung von nicht-erlaubten Schriftzeichen im Feedback-Text ###

| Schritt | Aktion                                                                                                                            | Erwartetes Ergebnis                                                                                                                                 | Ok/NOK | URL | Link to Issue |
| :--- |:----------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------| :--- | :--- | :--- |
| 1 | Öffne die Detailseite eines bereits gekauften Produkts.                                                                           | Die Produktseite lädt und der Bereich für das Feedback ist sichtbar.                                                                                | | | |
| 2 | Wähle eine Sternebewertung aus und gib einen Text mit nicht-erlaubten (nicht-ASCII) Zeichen ein (z. B. arabische Schriftzeichen). | Das System erkennt die unzulässigen Zeichen im Textfeld.                                                                                            | | | |
| 3 | Klicke auf den Button zum Absenden der Bewertung.                                                                                 | Das Absenden wird blockiert. Eine Fehlermeldung erscheint, dass nur Standard-Schriftzeichen erlaubt sind, und die Bewertung wird nicht gespeichert. | | | |

## Versandkosten (keine Versandkosten ab einem Bestellwert von 50€) ##

### Testfall 1: Anpassung der Versandkosten

| Schritt | Aktion                                                                                                 | Erwartetes Ergebnis                                                                                                       | Ok/NOK | URL | Link to Issue |
| :--- |:-------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------| :--- | :--- | :--- |
| 1 | Klicke in der oberen blauen Navigationsleiste auf „SHOP“.                                              | Die Produktauswahl wird fehlerfrei geöffnet.                                                                              | | | |
| 2 | Füge dem Warenkorb Produkte hinzu (über „Add to Cart“), bis der Gesamtwert der Artikel über 20€ liegt. | Die Produkte werden dem Warenkorb hinzugefügt und die Gesamtsumme steigt.                                                 | | | |
| 3 | Klicke auf das Warenkorb-Symbol oben rechts.                                                           | Der Warenkorb öffnet sich, zeigt die Artikel und die Versandkosten werden korrekt mit 0€ (versandkostenfrei) ausgewiesen. | | | |
| 4 | Entferne im Warenkorb so viele Artikel, bis der Gesamtwert der verbleibenden Produkte unter 20€ fällt. | Die Artikel werden entfernt, die Gesamtsumme sinkt und die Versandkosten werden automatisch auf 5,00 € angepasst.         | | | |

### Testfall 2: Versandkostenberechnung bei exakt 20,00 € Bestellwert (Grenzwert-Test)

| Schritt | Aktion | Erwartetes Ergebnis | Ok/NOK | URL | Link to Issue |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Klicke in der oberen blauen Navigationsleiste auf „SHOP“. | Die Produktauswahl wird fehlerfrei geöffnet. | | | |
| 2 | Füge dem Warenkorb gezielt Produkte hinzu, sodass der Gesamtwert der Artikel exakt 20,00 € beträgt. | Die Produkte werden hinzugefügt und die Gesamtsumme beträgt genau 20,00 €. | | | |
| 3 | Klicke auf das Warenkorb-Symbol oben rechts. | Der Warenkorb öffnet sich und die Versandkosten werden mit 0,00 € (versandkostenfrei) ausgewiesen. | | | |

### Testfall 3: Versandkostenberechnung knapp unter dem Grenzwert ###

| Schritt | Aktion | Erwartetes Ergebnis                                                                     | Ok/NOK | URL | Link to Issue |
| :--- | :--- |:----------------------------------------------------------------------------------------|:-------| :--- | :--- |
| 1 | Klicke in der oberen blauen Navigationsleiste auf „SHOP“. | Die Produktauswahl wird fehlerfrei geöffnet.                                            |        | | |
| 2 | Füge dem Warenkorb gezielt Produkte hinzu, sodass der Gesamtwert der Artikel knapp unter der Grenze zwischen 19,00 € und 19,99 € liegt. | Die Produkte werden hinzugefügt und der Gesamtwert der Bestellung liegt knapp unter 20€ |        | | |
| 3 | Klicke auf das Warenkorb-Symbol oben rechts. | Der Warenkorb öffnet sich und die Versandkosten werden korrekt mit 5,00 € berechnet.    |        | | |
