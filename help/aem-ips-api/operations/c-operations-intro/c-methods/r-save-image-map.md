---
description: Crea una nuova mappa immagine o modifica una mappa esistente.
solution: Experience Manager
title: saveImageMap
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 8%

---


# saveImageMap{#saveimagemap}

Crea una nuova mappa immagine o modifica una mappa esistente.

Sintassi

## Tipi di utenti autorizzati {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utente deve disporre dell’accesso in lettura e scrittura alla risorsa.

## Parametri {#section-64f7f5fd8f954fba9fa30eeee556863a}

**Input (saveImageMapParam)**

<table id="table_49649036F46941D2B1F28515674E533B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> L’handle dell’azienda con la mappa immagine da salvare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Il punto di manipolazione della risorsa immagine alla quale appartiene la mappa immagine. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> La maniglia della mappa immagine. Crea una mappa immagine se NULL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Nome della mappa immagine creata o salvata. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Scelta della forma di regione. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> regione  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Elenco di punti delimitato da virgole che definiscono la regione. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> action  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> <p>Il valore <span class="codeph"> href </span> associato alla mappa immagine come specificato nell'interfaccia IPS. </p> <p>Per ottenere il valore <span class="codeph"> href </span> , fai clic sull’immagine nell’interfaccia IPS, copia e incolla l’URL in questo elemento, quindi formatta l’URL IPS come URL corretto. Ad esempio, <span class="codeph"> &amp; </span> diventa <span class="codeph"> &amp;amp; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> posizione  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> L'ordine nell'elenco delle mappe immagine (l'asse Z). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> abilitato  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**Output (saveImageMapReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | Sì | La maniglia della mappa immagine nuova o modificata. |

## Esempi {#section-fdac488b640f427c8aa3d549c5032851}

Questo esempio di codice crea una nuova mappa immagine per una risorsa. Utilizza un tipo di forma determinato da una costante stringa di forma regione e restituisce un handle alla nuova mappa immagine.

**Request Contents (Richiesta contenuto)**

```
<saveImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <assetHandle>24266|1|17062</assetHandle> 
   <name>My Image Map</name> 
   <shapeType>Rectangle</shapeType> 
   <region>0,10,0,10</region> 
   <action>http://s7oslo.macromedia.com/scene7/browse/MoreInfo.jsp?assetID=24266&amp; 
   iRow=1&iRows=1&amp;strSearchType=image</action> 
   <position>0</position> 
</saveImageMapParam>
```

**Risposta**

```
<saveImageMapReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageMapHandle>34191|8|554</imageMapHandle> 
</saveImageMapReturn>
```

