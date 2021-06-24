---
description: Elimina una destinazione di zoom.
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 12%

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
| `*`companyHandle`*` | `xsd:string` | Sì | Handle della società a cui appartiene la destinazione dello zoom. |
| `*`zoomTargetHandle`*` | `xsd:string` | Sì | La maniglia della destinazione di zoom da eliminare. |

**Output (deleteZoomTargetParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempio {#section-a35857a5ca884357a879f7ba6cf985fe}

Questo esempio di codice elimina una destinazione di zoom da un&#39;azienda.

**Request Contents (Richiesta contenuto)**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Risposta**

Nessuno.
