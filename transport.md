---
id: transport
---

## Transport

De API v3 wordt aangeboden als eenvoudige HTTPS + XML API.

Er zijn 2 endpoints van belang:

* `/v3/resources?k=v`: deze url geeft een overzicht van alle dossiers die zijn aangemeld en die met het opvragende account zijn gedeeld. Elk dossier bevat een url naar de volledige dossier informatie. De resources zijn te filteren mbv 1 of meerdere key/value query parameters. Enkele voorbeelden:

  * `/v3/resources?client_bsn=9999999&gravida=2`
  * `/v3/resources?provider_account=naam`
  * `/v3/resources?client_birthdate=19880101`

* `/v3/register`: deze url wordt gebruikt om mbv POST data een aanmelding op de Hub te aan te melden of bij te werken. Deze aanmelding bevat de basis client en zwangerschaps gegevens (zie hierboven), en een lijst van 1 of meerdere team-leden welke toegang krijgen tot dit dossier.

Al het verkeer van en naar de Hub verloopt via SSL/HTTPS requests.

Het `/v3/resources` endpoint wordt opgevraagd mbv de GET methode.

Het `/v3/register` endpoint wordt op opgevraagd mbv de POST methode, en bevat de benodigde informatie over het dossier en delingen als XML bericht (zie verderop)
