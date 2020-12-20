---
description: Aggiunge un utente a un array di gruppi.
seo-description: Aggiunge un utente a un array di gruppi.
seo-title: addGroupMembership
solution: Experience Manager
title: addGroupMembership
topic: Scene7 Image Production System API
uuid: a8e25f27-c300-424d-83ac-e41bb4cb7964
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 9%

---


# addGroupMembership{#addgroupmembership}

Aggiunge un utente a un array di gruppi.

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
   <td colname="col4"> <p>Gestite l’utente di cui desiderate aggiungere l’iscrizione al gruppo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:HandleArray</span> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Array di handle per i gruppi a cui si desidera che la società appartenga. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (addGroupMembershipParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-f7a1f40c3d7a40ea964b29056c734d81}

In questo esempio viene aggiunto un gruppo a una società con ` *`groupHandleArray`*`. In questo esempio viene utilizzato un solo gruppo.

**Request Contents (Richiesta contenuto)**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Risposta**

Nessuno.
