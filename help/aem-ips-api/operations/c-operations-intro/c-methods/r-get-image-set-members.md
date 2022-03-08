---
description: Ottiene una matrice di membri che si trovano in un set di immagini.
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 14%

---

# getImageSetMembers{#getimagesetmembers}

Ottiene una matrice di membri che si trovano in un set di immagini.

Sintassi

## Tipi di utenti autorizzati {#section-eaa3a167fa77403ea1b374b05fff4ded}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Richiede l&#39;accesso in lettura all&#39;immagine e alla risorsa set di membri.

## Parametri {#section-a67ba98095574533980997c83ceaa316}

**Input (getImageSetMembersParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | L&#39;handle della società che contiene il set di immagini. |
| assetHandle | `xsd:string` | Sì | La maniglia della risorsa del set di immagini. |

**Output (getImageSetMembersReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| MemberArray | `types:ImageSetMemberArray` | No | Array di membri set di immagini. |

## Esempi {#section-888a9a78033346f39b171229de93dfa0}

Questo esempio di codice restituisce membri set di immagini specifici. La risposta restituisce una matrice vuota.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getImageSetMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>34195|22|927</ns1:assetHandle>
</ns1:getImageSetMembersParam>
```

**Risposta**

```java
<getImageSetMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray></memberArray>
</getImageSetMembersReturn>
```
