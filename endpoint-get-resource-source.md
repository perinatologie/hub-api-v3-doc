---
id: endpoint-get-resource-source
---

## [GET] /v3/resources/{resourceKey}/source


Om de daadwerkelijke bron data op te vragen kan via de `/source` sub-url alle benodigde informatie worden opgevraagd obv een resourceKey.

Een voorbeeld response:

```xml
<source>
  <api>v3</api>
  <url>https://api.example.com/dossierapi/162339584/G2%202015</url>
  <jwt>
      eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.
      eyJzdWIiOiIxMjM0NTY3ODkwIiwjbmFtZSI6IkpvaG4gRG9lIiwiYWRtaW4iOnRydWV9.
      TJVA95OrM7E2cBab30RMHrHDcEfxjoYZgeFONFh7HgQ
  </jwt>
  <provider>
    <account>xyz</account>
    <displayname>Praktijk XYZ</displayname>
  </provider>
</source>
```


Het source element bevat informatie welke gebruikt kan worden om de data op te halen bij de bron.
url: Directe URL naar het API end-point, inclusief alle parameters
api: De API versie momenteel actief bij de betreffende provider (v1 of v3)
jwt: JWT / JSON Web Token (zie details hieronder). Alleen igv API v3

Het JWT is cryptografisch ondertekend met de private key van de Hub. De provider kan voor bron-data verzoeken deze JWT te valideren mbv de public key van de Hub.

Het JWT bevat enkele “claims”, welke ook noodzakelijk zijn te controleren door de provider voor elk bron-data verzoek.

* iss: https://hub.perinatologie.nl
* aud: accountnaam van de Provider die bevraagd wordt
* sub: bsn van de client
* iat: huidige timestamp
* acc_name: account naam van de bevrager
* acc_display_name: display naam van de bevrager (ter info)
* nbf: huidige timestamp
* exp: huidige timestamp + verloop duur (configureerbaar, momenteel 1 uur).



