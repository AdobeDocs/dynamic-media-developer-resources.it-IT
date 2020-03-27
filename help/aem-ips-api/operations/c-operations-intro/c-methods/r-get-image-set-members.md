---
description: Ottiene un array di membri che si trovano in un set di immagini.
seo-description: Ottiene un array di membri che si trovano in un set di immagini.
seo-title: getImageSetMembers
solution: Experience Manager
title: getImageSetMembers
topic: Scene7 Image Production System API
uuid: b19c9fec-df92-42e1-9228-42cdf196fdfc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getImageSetMembers{#getimagesetmembers}

Ottiene un array di membri che si trovano in un set di immagini.

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
>Richiede l’accesso in lettura all’immagine e alla risorsa set di membri.

## Parametri {#section-a67ba98095574533980997c83ceaa316}

**Input (getImageSetMembersParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società che contiene il set di immagini. |
| ` *`assetHandle`*` | `xsd:string` | Sì | La maniglia della risorsa set di immagini. |

**Output (getImageSetMembersReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`MemberArray`*` | `types:ImageSetMemberArray` | No | Matrice di membri di set di immagini. |

## Esempi {#section-888a9a78033346f39b171229de93dfa0}

Questo esempio di codice restituisce membri specifici del set di immagini. La risposta restituisce un array vuoto.

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

