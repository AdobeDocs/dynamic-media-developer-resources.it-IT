---
description: Opacità. Specifica l'opacità del materiale.
solution: Experience Manager
title: opaca
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 7910228217db2c97dccd306ce464c69da53ee576
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# opac{#opac}

Opacità. Specifica l&#39;opacità del materiale.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>opacità del materiale (percentuale); 0...100 </p> </td> 
 </tr> 
</table>

Le seguenti combinazioni di materiale/oggetto supportano l&#39;opacità variabile:

* Tinte solide e texture ripetibili applicate agli oggetti di sovrapposizione texture.
* Materiali di rivestimento per finestre applicati agli oggetti telaio di copertura per finestre.
* Decalli applicati a oggetti di struttura o a pareti.

Se il materiale include un&#39;immagine con un canale alfa, `opac=` può essere utilizzato per rendere l&#39;immagine più trasparente, ma non più opaca.

## Proprietà {#section-352f7b82ede54159b6afb90ae4b559ec}

Attributo materiale. Ignorato se la selezione dell&#39;oggetto corrente o il materiale non supporta l&#39;opacità.

## Predefinito {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, per un materiale completamente opaco (se l&#39;immagine non include un canale alfa).
