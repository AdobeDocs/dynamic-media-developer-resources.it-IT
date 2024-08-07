---
description: Elimina una cartella.
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 6%

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
>L&#39;utente deve disporre dell&#39;accesso in lettura ed eliminazione alla cartella e a tutti i relativi elementi secondari.

## Parametri {#section-a793c98a481a4f26ab50bc69b16b57e7}

**Input (deleteFolderParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda a cui appartiene la cartella. |
| folderHandle | `xsd:string` | Sì | Handle della cartella da eliminare. |

**Output (deleteFolderParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-9d4617b322e8442d80e59be0f8714841}

Questo codice di esempio elimina una cartella dalla directory principale dell’azienda. Richiede un handle di cartella che è necessario ottenere da un&#39;altra operazione.

**Richiesta**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

Nessuno.
