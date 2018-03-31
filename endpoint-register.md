---
id: endpoint-register
---

## [POST] /v3/register

Dit end-point wordt gebruikt om een dossier aan te melden of bij te werken in de Hub.

De request-body bevat als post-data de nieuwe resource data. Een voorbeeld request body:

```
<?xml version="1.0" encoding="UTF-8"?>
<resource type="perinatologie/dossier">
  <property name="client_displayname">van der Jansen</property>
  <property name="client_bsn">162339584</property>
  <property name="client_birthdate">19861209</property>
  <property name="reference">2017001</property>
  <property name="gravida">2</property>
  <property name="para">0</property>
  <property name="start_at">20160103</property>
  <property name="end_at">20160409</property>
  <property name="edd">20160610</property>
</resource>
```

De Request Body bevat een lijst van properties van het dossier obv het resource type attribuut.
Details van deze properties komen overeen met de omschrijving in voorgaande hoofdstukken.

Een voorbeeld response:

```
<status key="Di3kDj3ale3984">OK</status>
```

Deze informatie geeft aan dat de resource correct is aangemeld op de hub, en wat de resource key is geworden. Deze kan in de applicatie worden opgeslagen voor toekomstige requests.

Wanneer dezelfde combinatie van gegevens (bsn, graviditeit) worden aangemeld via register, dan zal een eventueel bestaande resource worden geupdate ipv een nieuwe worden toegevoegd.
