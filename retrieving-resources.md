---
id: retrieving-resources
---

## Opvragen dossier bij doelsysteem

De hub geeft voor elke resource een source element terug. Deze source bevat een URL en een JWT. Deze informatie kan vervolgens gebruikt worden om een volledige en actuele versie van het dossier op te halen bij de provider van het betreffende resource.

De bevrager kan een HTTPS GET request uitvoeren naar de URL die ontvangen is door de Hub. Hieraan wordt als Query parameter de JWT toegevoegd.
Bijvoorbeeld:

* https://api.example.com/dossierapi/12345/G3?jwt=....

Zie voorgaande hoofdstukken voor de claims die in het JWT zijn ge-encodeerd.

Bij het implementeren van de provider api is het van groot belang dat de provider de JWT valideerd mbv de public key van de Hub, en dat daarnaast de claims ook worden gevalideerd.

* De waarde van iss moet https://hub.perinatologie.nl zijn.
* De waarde van aud moet het accountname van de provider zijn (anders kan een geldig JWT bij een andere provider worden gebruikt om data van een bepaald BSN op te vragen).
* De waarde van sub moet overeenkomen met het opgevraagde BSN in de URL (anders kan mbv een andere URL een andere resource data opgehaald worden)
* nbf en exp dienen gecontroleerd te worden (anders kan op een later tijdstip dezelfde JWT gebruikt worden). Het is te adviseren de API server klokken te synchroniseren.
* acc_name en acc_displayname zijn ter info voor logging bij de provider.

## Bron data formaat
Het formaat van de data die teruggegeven zal worden door de provider op de genoemde URL wordt bepaald door het resource type.

In geval van resource type `perinatologie/dossier` is dit het door leveranciers overeengekomen formaat “Form XML”.
