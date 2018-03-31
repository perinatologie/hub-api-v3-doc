---
id: endpoint-get-resource
---

## [GET] /v3/resources/{resourceKey}

Wanneer een resourceKey obv eerdere requests bekend is kan ook direct (zonder zoekopdracht) de laatste details van de resource opgevraagd worden.

Een voorbeeld response:

```xml
<resource type="perinatologie/dossier">
  <property name="key">jD83H4kXz</property>
  <property name="client_displayname">van der Jansen</property>
  <property name="client_bsn">162339584</property>
  <property name="client_birthdate">19861209</property>
  <property name="reference">G2 2016</property>
  <property name="gravida">2</property>
  <property name="para">0</property>
  <property name="start_at">20160103</property>
  <property name="end_at">20160409</property>
  <property name="edd">20160610</property>
  <property name="hub_registered_at">20160203</property>
  <property name="hub_provider_account">xyz</property>
</resource>
```
