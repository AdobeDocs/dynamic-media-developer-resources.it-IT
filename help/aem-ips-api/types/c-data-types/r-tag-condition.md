---
description: Definisce le condizioni di ricerca per i campi tag.
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
   <td colname="col3"> Handle campo tag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Dipende dal tipo di campo tag e dall’utilizzo del campo value o valueArray. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Se viene passato il valore <span class="codeph"></span>, <span class="codeph"> op</span> deve essere la costante di stringa Matches. La condizione corrisponde a qualsiasi risorsa associata al valore del tag. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Se <span class="codeph"> valueArray</span> viene passato, il campo op può essere la costante <span class="codeph"> MatchesAny</span> per i campi tag singoli o multivalore. Una condizione <span class="codeph"> MatchesAny</span> corrisponde a qualsiasi risorsa associata ad almeno uno dei valori di tag in <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">Per i campi tag con più valori, il campo op può essere impostato sulla costante <span class="codeph"> MatchesAll</span> con il campo valueArray</span> di <span class="codeph">. In questo caso, la condizione corrisponde solo alle risorse associate a tutti i valori di tag in <span class="codeph"> valueArray</span> (probabilmente in aggiunta ad altri valori di tag). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valore</span> </span> </td> 
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
