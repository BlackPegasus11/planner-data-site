# Planner-data-site

Data voor mijn planner (opdracht 3a, Informatica voor IoT 2).

Het bestand `db.json` bevat twee gekoppelde lijsten:

- **vakken**: id, naam, docent
- **taken**: id, titel, vak_id, deadline (JJJJ-MM-DD), klaar (true/false)

Elke taak verwijst met `vak_id` naar een bestaand vak.

## API

De data is online beschikbaar via [kdg-json-server](https://kdg-json-server.vercel.app/):

| Adres | Geeft |
|---|---|
| `/taken` | alle taken |
| `/taken/1` | taak met id 1 |
| `/vakken` | alle vakken |
| `/taken?vak_id=1` | taken van vak 1 |

Basisadres: `https://kdg-json-server.vercel.app/JOUW-GEBRUIKERSNAAM/JOUW-REPO`

## Gebruikt in

Een Flask-site die deze API aanroept met `requests` en de taken toont per vak.
