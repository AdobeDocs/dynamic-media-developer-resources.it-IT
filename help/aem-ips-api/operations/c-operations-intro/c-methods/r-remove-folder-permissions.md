---
description: Rimuove le autorizzazioni della cartella.
solution: Experience Manager
title: removeFolderPermissions
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 10830980-d504-4610-96c9-730937453256
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 9%

---

# removeFolderPermissions{#removefolderpermissions}

Rimuove le autorizzazioni della cartella.

Sintassi

## Tipi di utenti autorizzati {#section-bfa745624f9b43aaba6c226ac6700fe7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-7efa68377fd846219b906d354ae64ed3}

**Input (removeFolderPermissionsParam)**

<table id="table_15223256C63C4F008BDB1DF6F0AFE6A8"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> L'handle dell'azienda con cartelle con autorizzazioni da rimuovere. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Gestisci la cartella. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChildren</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> <p>Quando <span class="codeph"> true</span>: 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">La rimozione delle autorizzazioni viene propagata attraverso tutte le operazioni di autorizzazione delle cartelle. </li> 
     </ul> </p> <p>Quando <span class="codeph"> false</span>: 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">L'operazione influisce solo sulla cartella specificata. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (removeFolderPermissionsReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-04390f0ec7cc460cb5d34d518e33e7a5}

Questo esempio di codice rimuove le autorizzazioni da una cartella e dalle relative sottocartelle. Impostare `updateChildren` su `false` se è necessario rimuovere le autorizzazioni solo dalla cartella principale.

**Request Contents (Richiesta contenuto)**

```java
<removeFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <updateChildren>true</updateChildren>
</removeFolderPermissionsParam>
```

**Risposta**

Nessuno.
