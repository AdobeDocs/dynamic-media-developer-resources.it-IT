---
description: Restituisce le risorse da IPS.
seo-description: Restituisce le risorse da IPS.
seo-title: getAssets
solution: Experience Manager
title: getAssets
topic: Scene7 Image Production System API
uuid: ca06af8c-1753-4dfa-a7e6-1196ea769730
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 14%

---


# getAssets{#getassets}

Restituisce le risorse da IPS.

Sintassi

## Tipi di utenti autorizzati {#section-4673c1c9f4314160af8b165eb2dd20cc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Restituisce solo le risorse a cui l’utente ha accesso.

## Parametri {#section-bb9cf1ab19ea47acbd9ae58646dbe273}

**Input (getAssetParam)**

<table id="table_15CDEFC7F836411C80AA122E3A701C77"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obbligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>L'azienda gestisce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Impersona un utente specifico. Utilizzata solo dagli amministratori. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Filtrare per gruppo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Cartella principale per recuperare le cartelle e tutte le sottocartelle al livello foglia. Se esclusa, viene utilizzata la radice della società. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:StringArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Campi e sottocampi inclusi nella risposta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:StringArray</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Campi e sottocampi esclusi dalla risposta. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Outpub (getAssetsReturn)**

<table id="table_694932BBBD2C4167871380B2CF514BEA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obbligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:AssetArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array di risorse che corrispondono ai criteri del filtro. </p> </td> 
  </tr> 
 </tbody> 
</table>


