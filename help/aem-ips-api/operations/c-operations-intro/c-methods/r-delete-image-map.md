---
description: Elimina una mappa immagine.
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 9%

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

**Request Contents (Richiesta contenuto)**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Risposta**

Nessuno
