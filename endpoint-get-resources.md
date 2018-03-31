---
id: endpoint-list-resources
---

## [GET] /v3/resources?k=v

Dit end-point wordt gebruikt om obv bijvoorbeeld een BSN na te gaan welke dossiers er met de opvragende organisatie gedeeld zijn.

Mbv URL Query parameters kan er gefilterd worden op alle properties. Er kan dus ook gezocht worden op bijvoorbeeld geboortedatum of atermedatum (edd).

Een voorbeeld response:

```xml
<resources>
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
</resources>
```

Elk resource element bevat het attribuut ‘type’. Hierin wordt het resource type weergegeven, welke de ontvangende applicatie kan gebruiken om te bepalen of dit type resource verwerkt kan worden.

Elk resource response bevat alle properties zoals deze zijn vastgelegd in de Hub.
Toelichting op de properties van een resource van type perinatologie/dossier:
client_bsn: het BSN van de client
client_displayname: Volledige naam van de client
client_birthdate: Geboortedatum in YYYYMMDD formaat

* reference: Interne referentie voor aanmeldende organisatie. Bijvoorbeeld het zwangerschapsnummer of lvr nummer. Dit mag ook een interne ID zijn, echter tbv communicatie bij zorgverleners onderling is het wel te adviseren hier een bekende referentie voor te gebruiken.
* gravida: graviditeit
* para: pariteit
* start_at: Start zorg datum bij provider (YYYYDDMM)
* end_at: Einde zorg datum bij provider (YYYYDDMM) indien van toepassing

Let op: Andere resource typen kunnen dus andere properties bevatten.
