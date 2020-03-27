---
description: Imposta i valori di metadati per una risorsa specifica utilizzata con setAssetMetadata. Descrive le modifiche da apportare ai metadati.
seo-description: Imposta i valori di metadati per una risorsa specifica utilizzata con setAssetMetadata. Descrive le modifiche da apportare ai metadati.
seo-title: MetadataUpdate
solution: Experience Manager
title: MetadataUpdate
topic: Scene7 Image Production System API
uuid: 09d3940b-117d-4d83-8b12-e86520c9da34
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MetadataUpdate{#metadataupdate}

Imposta i valori di metadati per una risorsa specifica utilizzata con setAssetMetadata. Descrive le modifiche da apportare ai metadati.

>[!NOTE]
>
>Se viene passato il campo del valore singolo, il valore del tag della risorsa verrà reimpostato sul valore del tag specificato.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Handle del campo metadati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Valore di aggiornamento metadati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Valore dei metadati booleani (solo per i campi di tipo booleano). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Valore metadati lungo (solo per i campi con tipo int). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> Valore di metadati doppio (solo per i campi con tipo mobile). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Valore metadati data (solo per i campi con tipo data). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> addTagValueArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> <p>Aggiunge all’elenco dei valori dei tag esistenti per la risorsa. 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">I campi tag a valore singolo memorizzano solo l’ultimo valore. </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">Un campo di tag dizionario fisso restituisce un errore se il valore non è presente nel dizionario. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3">Sostituisce l’elenco di valori tag esistente per la risorsa. 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">I campi tag a valore singolo memorizzano solo l’ultimo valore. </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">Un campo di tag dizionario fisso restituisce un errore se il valore non è presente nel dizionario. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> Elimina i valori specificati dall'elenco dei valori tag della risorsa, se presente. </td> 
  </tr> 
 </tbody> 
</table>

