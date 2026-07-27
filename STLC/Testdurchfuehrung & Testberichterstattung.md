## Altersverifikation ##

### Testfall 1: Erfolgreiche Altersverifikation 18. Geburtstag (Grenzwert)

| Schritt | Aktion                                                                              | Erwartetes Ergebnis | Ok/NOK | URL | Link to Issue |
| :--- |:------------------------------------------------------------------------------------| :--- | :--- | :--- | :--- |
| 1 | Klicke in der oberen blauen Navigationsleiste auf „SHOP“.                           | Das Pop-up „Age Verification“ erscheint mit der Aufforderung zur Geburtsdatums-Eingabe. |OK |https://grocerymate.masterschool.com/store | |
| 2 | Gib das Geburtsdatum für den exakten heutigen 18. Geburtstag ein (bsp. 15-07-2008). | Das Datum wird im Eingabefeld korrekt angezeigt. |OK |https://grocerymate.masterschool.com/store | |
| 3 | Klicke auf den Button „Confirm“.                                                    | Das Pop-up schließt sich, der Shop öffnet sich und alkoholische Produkte sind sichtbar und kaufbar. |OK |https://grocerymate.masterschool.com/store | |

<img width="889" height="386" alt="Screenshot 2026-07-27 142104" src="https://github.com/user-attachments/assets/34f11c0a-875a-41fb-83eb-e6789cc9a58c" />
<img width="884" height="415" alt="Screenshot 2026-07-27 142131" src="https://github.com/user-attachments/assets/e61330f0-8161-4c90-aae8-d33eb3a857db" />
<img width="679" height="382" alt="Screenshot 2026-07-27 142141" src="https://github.com/user-attachments/assets/904aa0d9-7ba3-400d-afa7-e4bda6fe7052" />

### Testfall 2: Ungültiges Datumsformat ohne Trennzeichen (Negativtest)

Bemerkung: Erwartetes Ergebnis ist nicht eingetreten. Datumsformat wurde nicht als ungültig erkannt, stattdessen wurde die Eingabe als unter 18 Jahre bewertet. 

| Schritt | Aktion | Erwartetes Ergebnis | Ok/NOK | URL | Link to Issue |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Klicke in der oberen blauen Navigationsleiste auf „SHOP“. | Das Pop-up „Age Verification“ erscheint mit dem Text: „You need to be +18 to see some products. Please enter your birth date:“. |OK |https://grocerymate.masterschool.com/store
 | |
| 2 | Gib ein Geburtsdatum ohne Bindestriche oder Punkte ein (z. B. 27031987). | Das System erkennt das falsche Format und eine Fehlermeldung (z. B. „Format wird nicht unterstützt“) wird angezeigt. |NOK |https://grocerymate.masterschool.com/store | |
| 3 | Klicke auf den Button „Confirm“. | Der Zugriff auf den Shop bleibt gesperrt, bis ein gültiges Datumsformat eingegeben wird. |NOK |https://grocerymate.masterschool.com/store| |

<img width="889" height="386" alt="Screenshot 2026-07-27 142104" src="https://github.com/user-attachments/assets/34f11c0a-875a-41fb-83eb-e6789cc9a58c" />
<img width="857" height="371" alt="Screenshot 2026-07-27 143931" src="https://github.com/user-attachments/assets/cfb9965d-a0b2-4588-8ab4-7063f79f6845" />
<img width="659" height="316" alt="Screenshot 2026-07-27 143944" src="https://github.com/user-attachments/assets/d5b8b462-47d6-4505-b966-caf641db1b56" />

### Testfall 3: Absenden eines leeren Geburtsdatumsfeldes  ###

Bemerkung: Erwartetes Ergebnis ist nicht eingetreten. Leeres Eingabefeld für das Geburtsdatum wurde nicht erkannt, stattdessen bewertete das System die Eingabe als unter 18 Jahre. 
| Schritt | Aktion | Erwartetes Ergebnis | Ok/NOK | URL | Link to Issue |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Klicke in der oberen blauen Navigationsleiste auf „SHOP“. | Das Pop-up „Age Verification“ erscheint mit der Aufforderung zur Geburtsdatums-Eingabe. |OK|https://grocerymate.masterschool.com/store | |
| 2 | Lasse das Eingabefeld für das Geburtsdatum komplett leer. | Das Feld bleibt ohne Zeichen oder Zahlen. |OK |https://grocerymate.masterschool.com/store | |
| 3 | Klicke auf den Button „Confirm“. | Das System blockiert das Absenden. Das Pop-up schließt sich nicht und eine Fehlermeldung fordert zur Eingabe auf. |NOK|https://grocerymate.masterschool.com/store | |

<img width="889" height="386" alt="Screenshot 2026-07-27 142104" src="https://github.com/user-attachments/assets/34f11c0a-875a-41fb-83eb-e6789cc9a58c" />
<img width="659" height="316" alt="Screenshot 2026-07-27 143944" src="https://github.com/user-attachments/assets/d5b8b462-47d6-4505-b966-caf641db1b56" />

### Testfall 4: Sperrung eines minderjährigen Nutzers 

| Schritt | Aktion | Erwartetes Ergebnis | Ok/NOK | URL | Link to Issue |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Klicke in der oberen blauen Navigationsleiste auf „SHOP“. | Das Pop-up „Age Verification“ erscheint mit der Aufforderung zur Geburtsdatums-Eingabe. |OK |https://grocerymate.masterschool.com/store| |
| 2 | Gib ein Geburtsdatum ein, bei dem der Nutzer das 18. Lebensjahr noch nicht vollendet hat (z. B. das aktuelle Tagesdatum minus 15 Jahre). | Das Datum wird im Eingabefeld korrekt angezeigt. |OK |https://grocerymate.masterschool.com/store | |
| 3 | Klicke auf den Button „Confirm“. | Das System erkennt die Minderjährigkeit. Der Zugriff bleibt gesperrt und eine Hinweismeldung erscheint. |OK |https://grocerymate.masterschool.com/store | |

<img width="889" height="386" alt="Screenshot 2026-07-27 142104" src="https://github.com/user-attachments/assets/34f11c0a-875a-41fb-83eb-e6789cc9a58c" />
<img width="648" height="329" alt="Screenshot 2026-07-27 150814" src="https://github.com/user-attachments/assets/b9e295bd-31d3-4125-84dd-961de3f0ecdd" />
<img width="659" height="316" alt="Screenshot 2026-07-27 143944" src="https://github.com/user-attachments/assets/d5b8b462-47d6-4505-b966-caf641db1b56" />

