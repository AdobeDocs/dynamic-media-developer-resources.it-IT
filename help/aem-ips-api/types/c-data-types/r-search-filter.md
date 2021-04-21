---
description: Filtri che consentono di definire i criteri di ricerca per rendere le ricerche più efficienti.
solution: Experience Manager
title: SearchFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 1%

---


# SearchFilter{#searchfilter}

Filtri che consentono di definire i criteri di ricerca per rendere le ricerche più efficienti.

Sintassi

## Parametri {#section-4c611d9bbe0d418d882632605fc4d29d}

<table id="table_57CEE262A33A4E898C6AFB30C93FD874"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cartella</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Specifica la cartella da cercare. Lascia vuoto per cercare in tutta l’azienda. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Imposta su: 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> True</span>: Per cercare la cartella denominata e tutte le sottocartelle. </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> False</span>: Per cercare solo la cartella denominata. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">Elenco dei tipi di risorse che si desidera restituire in una ricerca. Ad esempio, <span class="codeph"> image</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3"> Specifica un tipo di risorsa da escludere da una ricerca. Ad esempio, immagine. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">Elenco dei sottotipi di risorse che dovranno essere restituiti in una ricerca. Ad esempio, per un <span class="codeph"> AssetSet</span>, è possibile cercare il sottotipo <span class="codeph"> MediaType</span> . </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> narrowSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Flag booleano facoltativo che specifica se restituire risorse senza sottotipo quando viene passato <span class="codeph"> assetSubTypeArray</span>. </p> <p>Se true, vengono restituite solo le risorse con uno dei sottotipi specificati. </p> <p>Se false, vengono restituite anche le risorse senza sottotipo. </p> <p>Le impostazioni predefinite sono false. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Imposta su: 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> True</span>: Per restituire solo le risorse originali. </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> False</span>: Per restituire il contenuto generato. Ad esempio, immagini da un PDF caricato. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Gestisci il progetto da cercare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Specifica: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> </span> MarkedForPublishper restituire solo le risorse pubblicate. </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> </span> NotMarkedForPublishper restituire solo le risorse non pubblicate. </li> 
    </ul> <p>Nota: Lascia vuoto per cercare i tipi di stato pubblicati <i>all</i> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Specifica: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> </span> È possibile restituire le risorse indipendentemente dal loro stato di rifiuto. </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> </span> NotInTrashto restituisce risorse 'normali'. </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> </span> InTrashper restituire le risorse dal cestino. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

