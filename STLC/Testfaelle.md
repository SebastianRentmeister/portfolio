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