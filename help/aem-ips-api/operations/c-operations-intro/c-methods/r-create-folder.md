---
title: createFolder
description: Consente di creare una cartella.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 16%

---

# [!DNL createFolder]{#createfolder}

Consente di creare una cartella.

>[!NOTE]
>
>La nuova cartella è subordinata alla cartella Immagini, anche se si specifica una `/` per indicare la radice della società.

Sintassi

## Tipi di utenti autorizzati {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L&#39;utente deve disporre dell&#39;accesso in lettura/scrittura alla cartella principale.

## Parametri {#section-c00d8d89cf114886a535056f2a1bf892}

**Input (createFolder)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | La Maniglia all&#39;azienda |
| folderPath | `xsd:string` | Sì | Cartella principale utilizzata per recuperare cartelle e sottocartelle a livello foglia. Se viene esclusa, viene utilizzata la radice della società. |

**Output (createFolderParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| folderHandle | `xsd:string` | Sì | Gestione della nuova cartella. |

## Esempi {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Questo codice di esempio crea una cartella nella directory principale di un&#39;azienda. La risposta restituisce l&#39;handle della nuova cartella creata.

**Request Contents (Richiesta contenuto)**

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**Risposta**

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```
