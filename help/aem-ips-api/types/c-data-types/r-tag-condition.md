---
description: Definisce ricerca condizioni per tag campi.
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---

# [!DNL TagCondition]{#tagcondition}

Definisce ricerca condizioni per tag campi.

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
   <td colname="col1"> <span class="codeph"><span class="varname"> Gestione</span> campo </span> </td> 
   <td colname="col2"> <span class="codeph"> XSD:stringa</span> </td> 
   <td colname="col3"> Handle del campo tag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> XSD:stringa</span> </td> 
   <td colname="col3">Dipende dal tipo di campo tag e dall'utilizzo del campo value o valueArray. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Se <span class="codeph"> il valore</span> viene passato, <span class="codeph"> op</span> deve essere la costante di stringa Corrispondenze. La condizione corrisponde a qualsiasi risorsa associato al valore tag. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Se <span class="codeph"> viene passato valueArray</span> , il campo op può essere la costante <span class="codeph"> MatchesAny</span> per i campi tag a valore singolo o multivalore. Una <span class="codeph"> condizione MatchesAny</span> corrisponde a qualsiasi risorsa associato ad almeno uno dei valori tag in <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">Per i campi tag multivalore, il campo op può essere impostato sulla costante <span class="codeph"> MatchesAll</span> con il <span class="codeph"> campo valueArray</span> . In questo caso, la condizione corrisponde solo ai risorse associati a tutti i valori tag in <span class="codeph"> valueArray</span> (possibilmente in aggiunta ad altri valori tag). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> valore</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> XSD:stringa</span> </td> 
   <td colname="col3"> Un valore corrispondente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> Più valori corrispondenti. </td> 
  </tr> 
 </tbody> 
</table>
