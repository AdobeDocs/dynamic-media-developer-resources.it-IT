---
description: Filtri che consentono di definire criteri di ricerca per rendere più efficienti le ricerche.
seo-description: Filtri che consentono di definire criteri di ricerca per rendere più efficienti le ricerche.
seo-title: SearchFilter
solution: Experience Manager
title: SearchFilter
topic: Scene7 Image Production System API
uuid: 85a434d3-51a5-4e68-901e-70585c0e8b20
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SearchFilter{#searchfilter}

Filtri che consentono di definire criteri di ricerca per rendere più efficienti le ricerche.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> cartella</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Specificate la cartella in cui desiderate eseguire la ricerca. Lasciate vuoto per effettuare ricerche all’interno e all’intera società. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> include sottocartelle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Impostate su: 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> Vero</span>: Per cercare nella cartella denominata e in tutte le sottocartelle. </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> False</span>: Per cercare solo nella cartella denominata. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> assetTypeArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">Elenco dei tipi di risorse che si desidera restituire in una ricerca. Ad esempio, <span class="codeph"> image</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3"> Specificate un tipo di risorsa da escludere da una ricerca. Ad esempio, image. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> assetSubTypeArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">Elenco dei sottotipi di risorse da restituire in una ricerca. Ad esempio, per un <span class="codeph"> AssetSet</span>, potete cercare il sottotipo <span class="codeph"> MediaType</span> . </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> rigorosoSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Flag booleano facoltativo che specifica se restituire risorse senza sottotipo quando viene passato <span class="codeph"> assetSubTypeArray</span> . </p> <p>Se true, vengono restituite solo le risorse con uno dei sottotipi specificati. </p> <p>Se è false, vengono restituite anche le risorse senza sottotipo. </p> <p>I valori predefiniti sono falsi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Impostate su: 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> Vero</span>: Per restituire solo le risorse originali. </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> False</span>: Per restituire il contenuto generato. Ad esempio, immagini da un PDF caricato. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Gestite il progetto da cercare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Specificate: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> ContrassegnatoPerPubblicare</span> per restituire solo le risorse pubblicate. </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> NotMarkedForPublish</span> per restituire solo risorse non pubblicate. </li> 
    </ul> <p>Nota: Lasciate vuoto per cercare <i>tutti</i> i tipi di stato pubblicati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Specificate: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> Qualsiasi</span> risorsa per restituire le risorse indipendentemente dal loro stato di cestino. </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> NotInTrash</span> per restituire risorse "normali". </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> InCestino</span> per restituire le risorse dal cestino. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

