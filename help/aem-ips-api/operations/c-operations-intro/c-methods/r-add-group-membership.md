---
description: Aggiunge un utente a una matrice di gruppi.
solution: Experience Manager
title: addGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 9%

---


# addGroupMembership{#addgroupmembership}

Aggiunge un utente a una matrice di gruppi.

Sintassi

## Tipi di utenti autorizzati {#section-fe950150718a474d8df30d0f4453c022}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-e250f6ddb13646808c6a8860b6442bc5}

**Input (addGroupMembershipParam)**

<table id="table_71AD8902E4854CA5A12379DBA4DF17C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Gestisci l'utente di cui desideri aggiungere l'iscrizione al gruppo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:HandleArray</span> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Array di handle ai gruppi a cui si desidera che la società appartenga. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (addGroupMembershipParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-f7a1f40c3d7a40ea964b29056c734d81}

Questo esempio aggiunge un gruppo a una società con `*`groupHandleArray`*`. In questo esempio viene utilizzato un solo gruppo.

**Request Contents (Richiesta contenuto)**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Risposta**

Nessuno.
