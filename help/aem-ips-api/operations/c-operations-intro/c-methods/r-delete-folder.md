---
description: Elimina una cartella.
seo-description: Elimina una cartella.
seo-title: deleteFolder
solution: Experience Manager
title: deleteFolder
uuid: 76af65fb-86ef-43e2-bfec-3682acf0afe6
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 8%

---


# deleteFolder{#deletefolder}

Elimina una cartella.

Sintassi

## Tipi di utenti autorizzati {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utente deve disporre dell’accesso in lettura ed eliminazione alla cartella e a tutti i relativi elementi secondari.

## Parametri {#section-a793c98a481a4f26ab50bc69b16b57e7}

**Input (deleteFolderParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società a cui appartiene la cartella. |
| `*`folderHandle`*` | `xsd:string` | Sì | L&#39;handle della cartella da eliminare. |

**Output (deleteFolderParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-9d4617b322e8442d80e59be0f8714841}

Questo codice di esempio elimina una cartella dalla radice della società. Richiede un handle di cartella, che è necessario ottenere da un&#39;altra operazione.

**Request Contents (Richiesta contenuto)**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

Nessuno.
