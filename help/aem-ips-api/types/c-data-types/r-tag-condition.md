---
description: Definisce le condizioni di ricerca per i campi tag.
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 2%

---


# TagCondition{#tagcondition}

Definisce le condizioni di ricerca per i campi tag.

Sintassi

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Maniglia del campo di tag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Dipende dal tipo di campo tag e dall’utilizzo del campo value o valueArray. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Se viene passato <span class="codeph"> value</span>, <span class="codeph"> op</span> deve essere la stringa costante Matches. La condizione corrisponde a qualsiasi risorsa associata al valore del tag. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Se viene passato <span class="codeph"> valueArray</span>, il campo op può essere la costante <span class="codeph"> MatchesAny</span> per campi tag singoli o multivalore. Una condizione <span class="codeph"> MatchesAny</span> corrisponde a qualsiasi risorsa associata ad almeno uno dei valori tag in <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">Per i campi di tag con più valori, il campo op può essere impostato sulla costante <span class="codeph"> MatchesAll</span> con il campo <span class="codeph"> valueArray</span>. In questo caso, la condizione corrisponde solo alle risorse associate a tutti i valori tag in <span class="codeph"> valueArray</span> (possibilmente in aggiunta ad altri valori tag). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Un valore corrispondente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> Più valori corrispondenti. </td> 
  </tr> 
 </tbody> 
</table>

