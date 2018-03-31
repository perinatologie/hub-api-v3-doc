---
id: endpoint-4
---

## [GET] /v3/resources/{resourceKey}/shares

Dit end-point geeft een actueel overzicht van alle accounts waarmee de betreffende resource is gedeeld.

Een voorbeeld response:

```
<shares>
  <share>
    <resourceKey>jD83H4kXz</resourceKey>
    <granteeName>account-a</granteeName>
    <granteeDisplayName>Account B</granteeDisplayName>
    <permission>full</permission>
  </share>
  <share>
    <resourceKey>jD83H4kXz</resourceKey>
    <granteeName>account-b</granteeName>
    <granteeDisplayName>Account B</granteeDisplayName>
    <permission>full</permission>
  </share>
</shares>
```
