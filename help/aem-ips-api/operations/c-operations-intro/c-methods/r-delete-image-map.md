---
description: Elimina una mappa immagine.
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
TQID: 'https://experienceleague.adobe.com/6r-EiZLM0tRUpzoTJyTt3rAkyABfNH9DQvDJq-XsqPY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 93
ht-degree: 7%

---

# deleteImageMap{#deleteimagemap}

Elimina una mappa immagine.

Sintassi

## Tipi di utenti autorizzati {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utente deve disporre dell’accesso in lettura e scrittura alla risorsa.

## Parametri {#section-28de12bab79045a5977c68855e37ae3d}

**Input (deleteImageMapParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle della società contenente la mappa immagine da eliminare. |
| imageMapHandle | `xsd:string` | Sì | Handle della mappa immagine da eliminare. |

**Output (deleteImageMapParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Questo esempio di codice elimina una mappa immagine da un&#39;azienda. È necessario ottenere l&#39;handle della mappa immagine da un&#39;altra operazione.

**Richiesta**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Risposta**

Nessuno
