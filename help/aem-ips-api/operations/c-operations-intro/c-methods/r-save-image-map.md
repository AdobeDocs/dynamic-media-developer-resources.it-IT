---
description: Crea una nuova mappa immagine o modifica una mappa esistente.
solution: Experience Manager
title: saveImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 91e40549-9b26-41f2-a3ab-7e9bec8f9ba7
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 7%

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Handle per l'azienda con la mappa immagine che si desidera salvare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Handle della risorsa immagine a cui appartiene la mappa immagine. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Handle della mappa immagine. Crea una mappa immagine se NULL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nome </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Nome della mappa immagine creata o salvata. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ShapeType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Scelta della forma Regione. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> area </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Un elenco delimitato da virgole di punti che definiscono la regione. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> azione </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> <p>Il valore <span class="codeph"> href </span> associato alla mappa immagine come specificato nell'interfaccia IPS. </p> <p>Per ottenere il valore <span class="codeph"> href </span>, fare clic sull'immagine nell'interfaccia IPS, copiare e incollare l'URL in questo elemento, quindi formattare l'URL IPS come URL corretto. Ad esempio, <span class="codeph"> e </span> diventano <span class="codeph"> &amp;amp; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> posizione </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> L'ordine nell'elenco delle mappe immagine (l'asse Z). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> abilitato </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**Output (saveImageMapReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| imageMapHandle | `xsd:string` | Sì | Handle della mappa immagine nuova o modificata. |

## Esempi {#section-fdac488b640f427c8aa3d549c5032851}

Questo esempio di codice crea una nuova mappa immagine per una risorsa. Utilizza un tipo di forma determinato da una costante stringa di forma area e restituisce un punto di manipolazione nella nuova mappa immagine.

**Richiesta**

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
