---
description: Ottiene una matrice di membri che si trovano in un set di immagini.
seo-description: Ottiene una matrice di membri che si trovano in un set di immagini.
seo-title: getImageSetMembers
solution: Experience Manager
title: getImageSetMembers
uuid: b19c9fec-df92-42e1-9228-42cdf196fdfc
feature: Dynamic Media Classic, SDK/API, Set di immagini
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 12%

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
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società che contiene il set di immagini. |
| `*`assetHandle`*` | `xsd:string` | Sì | La maniglia della risorsa del set di immagini. |

**Output (getImageSetMembersReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`MemberArray`*` | `types:ImageSetMemberArray` | No | Array di membri set di immagini. |

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

