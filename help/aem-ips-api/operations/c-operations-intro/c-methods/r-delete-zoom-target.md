---
description: Elimina una destinazione di zoom.
seo-description: Elimina una destinazione di zoom.
seo-title: deleteZoomTarget
solution: Experience Manager
title: deleteZoomTarget
topic: Scene7 Image Production System API
uuid: 01a9321f-89a9-4263-937b-b0b49fe2fb81
translation-type: tm+mt
source-git-commit: d3766bba78cd1051538ff6a94f61ba61e989f1a5

---


# deleteZoomTarget{#deletezoomtarget}

Elimina una destinazione di zoom.

## Tipi di utenti autorizzati {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utente deve disporre dell’accesso in lettura e scrittura alla risorsa.

## Parametri {#section-225330a45e7a408f8375e084677d9cb1}

**Input (deleteZoomTargetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | Handle della società a cui appartiene la destinazione di zoom. |
| ` *`zoomTargetHandle`*` | `xsd:string` | Sì | La maniglia della destinazione di zoom da eliminare. |

**Output (deleteZoomTargetParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempio {#section-a35857a5ca884357a879f7ba6cf985fe}

Questo esempio di codice elimina una destinazione di zoom da una società.

**Request Contents (Richiesta contenuto)**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Risposta**

Nessuno.
