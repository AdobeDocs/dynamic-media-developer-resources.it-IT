---
description: Elimina una destinazione di zoom.
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 8%

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
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda a cui appartiene il target di zoom. |
| zoomTargetHandle | `xsd:string` | Sì | Handle della destinazione di zoom da eliminare. |

**Output (deleteZoomTargetParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempio {#section-a35857a5ca884357a879f7ba6cf985fe}

Questo esempio di codice elimina un target di zoom da un’azienda.

**Richiesta**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Risposta**

Nessuno.
