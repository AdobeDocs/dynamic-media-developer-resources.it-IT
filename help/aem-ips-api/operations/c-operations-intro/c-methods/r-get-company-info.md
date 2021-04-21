---
description: Restituisce informazioni sulla società specificata, tra cui l'handle della società, il nome della società, il percorso principale e la data di scadenza. È necessario specificare companyHandle o companyName di cui si desidera recuperare le informazioni.
solution: Experience Manager
title: getCompanyInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 6%

---


# getCompanyInfo{#getcompanyinfo}

Restituisce informazioni sulla società specificata, tra cui l&#39;handle della società, il nome della società, il percorso principale e la data di scadenza. È necessario specificare companyHandle o companyName di cui si desidera recuperare le informazioni.

Sintassi

## Tipi di utenti autorizzati {#section-74f20fb8602e4f96810795bc4b6f7fdf}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-7dec8871c89a414c9f066adade1831d8}

**Input (getCompanyInfoParam)**

<table id="table_DD2688C9DA9F49C9ABCA24944829B3E5"> 
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
   <td colname="col3"> <p>È necessario <span class="codeph"> <span class="varname"> companyHandle</span> </span> o <span class="codeph"> <span class="varname"> companyName</span> </span>. </p> </td> 
   <td colname="col4"> <p>L'handle dell'azienda di cui si desidera ottenere le informazioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>È necessario <span class="codeph"> <span class="varname"> companyHandle</span> </span> o <span class="codeph"> <span class="varname"> companyName</span> </span>. </p> </td> 
   <td colname="col4"> <p>Nome dell'azienda di cui si desidera ottenere le informazioni. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getCompanyInfoReturn)**

<table id="table_634D4E274BA7494C9C917FD244286F0D"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:Azienda</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Gestisci e altre informazioni descrittive sull'azienda. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempi {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

Questo esempio di codice restituisce tutte le informazioni su un&#39;azienda utilizzando un nome e un handle dell&#39;azienda. Restituisce dati simili alla risposta ricevuta al momento della creazione di una società.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getCompanyInfoParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:getCompanyInfoParam>
```

**Risposta**

```java
<ns1:getCompanyInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:getCompanyInfoReturn>
```

