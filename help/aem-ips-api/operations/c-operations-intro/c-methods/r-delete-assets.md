---
description: Elimina più risorse.
seo-description: Elimina più risorse.
seo-title: deleteAssets
solution: Experience Manager
title: deleteAssets
topic: Scene7 Image Production System API
uuid: ed446ebf-4a3d-4ee8-9ab3-596b1f05e5f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 10%

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
   <td colname="col4"> <p>L’handle della società a cui appartengono le risorse. </p> </td> 
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
   <td colname="col4"> <p>Numero di risorse eliminate correttamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> warningCount</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Risorse che generavano un avviso quando l'operazione tentava di eliminarle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> errorCount</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Risorse che hanno generato un errore durante il tentativo di eliminazione dell'operazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:AssetOperationFaultArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array di dettagli associati alle risorse che generavano un avviso quando l'operazione tentava di eliminarle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:AssetOperationFaultArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Array di dettagli associati alle risorse che generavano un errore quando l'operazione tentava di eliminarle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempi {#section-aaad1933bf86479eb6cb476cec7d4587}

Questo esempio di codice invia un handle a una società e un array di handle di risorse in una richiesta `deleteAssetsParam` al server dei servizi Web. `deleteAssetsReturn` restituisce un conteggio di successo pari a 2, a indicare che entrambe le risorse sono state eliminate.

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

