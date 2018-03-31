---
id: endpoint-share-add
---

## [GET] /v3/resources/{resourceKey}/add-share/{accountName}/{permission}

Nadat een resource is aangemeld kan deze worden gedeeld met andere Hub accounts.

De URL bevat een accountName waarmee het betreffende resource gedeeld mag worden. De `permission` parameter bevat de gegevens die aangeven wat er precies gedeeld mag worden igv selectief delen. Standaard kan hier de permission `full` worden gebruikt.
