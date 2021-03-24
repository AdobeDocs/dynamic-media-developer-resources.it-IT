---
description: Imposta l’elenco delle risorse associate a un set di immagini.
solution: Experience Manager
title: setImageSetMembers
feature: Dynamic Media Classic, SDK/API, Set di immagini
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 8%

---


# setImageSetMembers{#setimagesetmembers}

Imposta l’elenco delle risorse associate a un set di immagini.

Questa operazione ignora il parametro `pageReset` per `ImageSets` e `SpinSets` e forza il valore su true.

## Tipi di utenti autorizzati {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utente deve avere accesso in lettura e scrittura alla risorsa set di immagini e accesso in lettura a ogni risorsa membro.

## Parametri {#section-2f46efcd24c648aeacba738509426e46}

**Input (setImageSetMembersParam)**

<table id="table_0CBBB65BCEFD4125A4069A080DFC873A"> 
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
   <td colname="col4"> <p>Tratta l'azienda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Maniglia del set di immagini. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> MemberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Array di membri di risorse appartenenti al set di immagini. </td> 
  </tr> 
 </tbody> 
</table>

**Output (setImageSetMembersReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-7b87219034464aa98524178ccee27738}

Questo esempio di codice utilizza una matrice di membri per impostare i membri di un set di immagini.

**Request Contents (Richiesta contenuto)**

```java
<setImageSetMembersParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>34205|22|929</assetHandle>
   <memberArray>
      <items>
         <assetHandle>24266|1|17062</assetHandle>
         <pageReset>true</pageReset>
      </items>
   </memberArray>
</setImageSetMembersParam>
```

**Risposta**

Nessuno.
