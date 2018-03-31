---
id: index
---

# Hub API v3
## Implementatie handleiding

### Inleiding

De Hub is een initiatief ter bevordering van het delen van gegevens in de geboortezorg. Om dit doel te bereiken staat de Hub open voor alle zorgaanbieders en software leveranciers.

Zorgaanbieders kunnen eenvoudig toegang tot de actuele versies van het dossier ontsluiten, direct vanuit hun software applicatie. Er wordt dus niet gewerkt met ‘berichten’, welke slechts een snapshot zijn van een bepaald moment. Middels de Hub kunnen vragende zorgaanbieders altijd de meest actuele gegevens raadplegen.

### Hoe werkt het?

Het concept is erg eenvoudig: Er kunnen dossiers worden aangemeld en dossiers kunnen worden gezocht. Na het vinden van een betreffend dossier kunnen de actuele gegevens worden opgevraagd bij de bron.

#### Dossiers aanmelden

Aangesloten organisaties en personen (hub accounts) kunnen dossiers (resources) aanmelden op de Hub, en bij deze aanmelding vastleggen welke andere accounts toegang krijgen tot het betreffende dossier (shares).

Een aanmelding bevat de volgende informatie:

Client gerelateerde elementen:

* client_bsn: Burger Service Nummer
* client_displayname: Volledige naam van de client
* client_birthdate: Geboortedatum (in formaat YYYYMMdd)

Zwangerschap gerelateerde elementen:

* reference: Interne referentie van aanmeldende provider (zwangerschapsnummer in bronsysteem)
* gravida: Graviditeit
* para: Pariteit
* edd: Aterme datum
* start_at: Start datum zorg bij provider
* end_at: Eind datum zorg bij provider

#### Dossiers zoeken

De Hub bevat alleen de basis gegevens van een dossier zodat andere accounts het dossier kunnen vinden. De Hub bevat niet het dossier zelf, slechts een verwijzing hiernaar bij het bron-systeem.

De beschikbare dossiers kunnen opgevraagd worden obv verschillende eigenschappen van een dossier. In veel gevallen is dit het BSN van de client. Als reactie op de zoekopdracht volgt een lijst met dossiers die andere organisaties hebben aangemeld, en gedeeld hebben met het opvragende account.
