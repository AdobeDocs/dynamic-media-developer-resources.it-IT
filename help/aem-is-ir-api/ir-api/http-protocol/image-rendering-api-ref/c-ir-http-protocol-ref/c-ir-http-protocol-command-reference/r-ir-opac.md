---
title: opac
description: Opacità. Specifica l'opacità del materiale.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# opac{#opac}

Opacità. Specifica l&#39;opacità del materiale.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> Valore <span class="varname"> </span> </p> </td> 
  <td class="stentry"> <p>Opacità materiale (percentuale); 0...100 </p> </td> 
 </tr> 
</table>

Le seguenti combinazioni materiale/oggetto supportano l&#39;opacità variabile:

* Colore solido e texture ripetibili applicate agli oggetti di sovrapposizione textural.
* Materiali di rivestimento per finestre applicati agli oggetti di rivestimento per finestre.
* Decalcomanie applicate a oggetti textural o wall.

Se il materiale include un&#39;immagine con un canale alfa, è possibile utilizzare `opac=` per rendere l&#39;immagine più trasparente, ma non più opaca.

## Proprietà {#section-352f7b82ede54159b6afb90ae4b559ec}

Attributo materiale. Ignorato se la selezione dell&#39;oggetto corrente o il materiale non supporta l&#39;opacità.

## Predefinito {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, per un materiale completamente opaco (se l&#39;immagine non include un canale alfa).
