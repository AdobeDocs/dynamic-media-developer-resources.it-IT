---
description: Restituisce le risorse in base a un array di nomi di risorse.
seo-description: Restituisce le risorse in base a un array di nomi di risorse.
seo-title: getAssetsByName
solution: Experience Manager
title: getAssetsByName
topic: Scene7 Image Production System API
uuid: e86b3b16-ad93-4f70-9f59-b72395513c4c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssetsByName{#getassetsbyname}

Restituisce le risorse in base a un array di nomi di risorse.

Sintassi

## Tipi di utenti autorizzati {#section-754790841ea242d5ae8bedd587d7730e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Restituisce solo le risorse a cui l&#39;utente ha accesso in lettura.

## Parametri {#section-f64e93c127b84a29aa3bf2fdd916cca9}

**Input (getAssetsByNameParam)**

<table id="table_CE7B503B0E074719A523B458DF3A7286"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obbligatorio </th> 
   <th colname="col4" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> L'handle della società. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Fornisce l'accesso come altro utente. Disponibile solo per gli amministratori. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Utilizzato per filtrare in base a un gruppo specifico. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nameArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Array di nomi di risorse da recuperare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> assetTypeArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Array di tipi di risorse consentiti per le risorse recuperate. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Array di tipi di risorse esclusi per le risorse recuperate. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> assetSubTypeArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Array di sottotipi di risorse consentiti per le risorse recuperate. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> rigorosoSubTypeCheck</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Se <span class="codeph"> true</span> e <span class="codeph"> assetSubTypeArray</span> non sono vuoti, vengono restituite solo le risorse i cui sottotipi si trovano in <span class="codeph"> assetSubTypeArray</span> . </p> <p>Se è <span class="codeph"> false</span>, vengono incluse anche le risorse senza sottotipo definito. </p> <p>The default value is <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Contiene un elenco di campi e sottocampi inclusi nella risposta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Contiene un elenco di campi e sottocampi esclusi dalla risposta. </td> 
  </tr> 
 </tbody> 
</table>

**Output (getAssetsByNameReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`assetArray`*` | `types:AssetArray` | No | Array di risorse che corrispondono ai criteri del filtro. |

## Esempi {#section-3b7447398e574c88aeaf8ca159cc78dd}

Questo esempio di codice restituisce due risorse di tipo immagine.

**Request Contents (Richiesta contenuto)**

```java
<getAssetsByNameParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <nameArray>
      <items>B010</items>
      <items>IMG_0103</items>
   </nameArray>
   <assetTypeArray>
      <items>Image</items>
   </assetTypeArray>
</getAssetsByNameParam>
```

**Risposta**

```java
<getAssetsByNameReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <assetArray>
      <items>
         <assetHandle>a|210</assetHandle>
         <type>Image</type>
         <name>B010</name>
         ...</items>
      <items>
         <assetHandle>a|189</assetHandle>
         <type>Image</type>
         <name>IMG_0103</name>
         ...
      </items>
   </assetArray>
</getAssetsByNameReturn>
```

