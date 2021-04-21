---
description: Elimina più risorse.
solution: Experience Manager
title: deleteAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 9%

---


# deleteAssets{#deleteassets}

Elimina più risorse.

Sintassi

## Tipi di utenti autorizzati {#section-a6bc555b8ac840c98835b73fbf838d70}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-4dc888e77d974ac794b553616dd11e86}

**Input (deleteAssetsParam)**

<table id="table_AAA6845769DB4B129C8A660D0CBA348A"> 
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
   <td colname="col4"> <p>L'handle dell'azienda a cui appartengono le risorse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Matrice di risorse da eliminare. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (deleteAssetsParam)**

<table id="table_0C6D8D51A79248ACA2022DBB754A9B9C"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> successCount</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Numero di risorse eliminate. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> warningCount</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Le risorse che generavano un avviso quando l’operazione tentava di eliminarle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> errorCount</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Le risorse che generavano un errore quando l’operazione tentava di eliminarle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:AssetOperationFaultArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array di dettagli associati alle risorse che hanno generato un avviso quando l’operazione tentava di eliminarle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:AssetOperationFaultArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array di dettagli associati alle risorse che hanno generato un errore quando l’operazione tentava di eliminarle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempi {#section-aaad1933bf86479eb6cb476cec7d4587}

Questo esempio di codice invia un handle a un&#39;azienda e una matrice di handle di risorse in una richiesta `deleteAssetsParam` al server dei servizi Web. `deleteAssetsReturn` restituisce un conteggio di successo di 2, che indica che entrambe le risorse sono state eliminate.

**Request Contents (Richiesta contenuto)**

```java
<deleteAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</deleteAssetsParam>
```

**Risposta**

```java
<deleteAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</deleteAssetsReturn>
```

