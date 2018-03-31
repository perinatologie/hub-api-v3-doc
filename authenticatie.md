---
id: authenticatie
---

## Authenticatie

Om aan te sluiten op de Hub heeft een organisatie een eigen Hub Account nodig. Deze zijn te verkrijgen via [www.perinatologie.nl](https://www.perinatologie.nl)

Voor elk Hub Account kunnen 1 of meerdere API Keys worden uitgegeven. Een API Key geeft toegang tot de dossiers die gedeeld zijn met het bijbehorende account.

Een API key bevat zowel een `key` als een `secret`. De key kan zichtbaar zijn voor derden. Het secret dient geheim te blijven bij de eigenaar van het account.

Mbv de api key en secret kan een applicatie requests plaatsen op de Hub mbv HTTP Basic Auth via een SSL verbinding.
