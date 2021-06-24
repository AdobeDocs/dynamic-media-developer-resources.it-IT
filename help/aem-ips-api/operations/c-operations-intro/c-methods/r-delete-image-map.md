---
description: Elimina una mappa immagine.
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 10%

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
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società che contiene la mappa immagine da eliminare. |
| `*`imageMapHandle`*` | `xsd:string` | Sì | La maniglia della mappa immagine da eliminare. |

**Output (deleteImageMapParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Questo esempio di codice elimina una mappa immagine da un&#39;azienda. È necessario ottenere la maniglia della mappa immagine da un’altra operazione.

**Request Contents (Richiesta contenuto)**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Risposta**

Nessuno
