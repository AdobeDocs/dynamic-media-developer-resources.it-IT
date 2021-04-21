---
description: Esegue un processo specifico.
solution: Experience Manager
title: executeJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 12%

---


# executeJob{#executejob}

Esegue un processo specifico.

Sintassi

## Tipi di utenti autorizzati {#section-8199e8599ea64e7097a2acb633417b15}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-2c61b2bffcf9479a9391f2c13fdf7d53}

**Input (executeJobParam)**

<table id="table_FA410513908F4084A21A5F0A9431006C"> 
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
   <td colname="col4"> <p>L'handle dell'azienda a cui appartiene il lavoro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> jobHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>L'handle del processo da eseguire. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (executeJobReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-96f71aa58a954293b9a98ff96d86f232}

Questo esempio di codice esegue un processo pianificato per l&#39;esecuzione in IPS.

**Request Contents (Richiesta contenuto)**

```java
<executeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</executeJobParam>
```

**Risposta**

Nessuno.
