---
description: Elimina una mappa immagine.
seo-description: Elimina una mappa immagine.
seo-title: deleteImageMap
solution: Experience Manager
title: deleteImageMap
topic: Dynamic Media Image Production System API
uuid: 0abdf72c-f445-41d0-bd88-63b7ad1359d5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
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
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle della società che contiene la mappa immagine da eliminare. |
| `*`imageMapHandle`*` | `xsd:string` | Sì | La maniglia della mappa immagine da eliminare. |

**Output (deleteImageMapParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Questo esempio di codice elimina una mappa immagine da una società. È necessario ottenere la maniglia della mappa immagine da un’altra operazione.

**Request Contents (Richiesta contenuto)**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Risposta**

Nessuno
