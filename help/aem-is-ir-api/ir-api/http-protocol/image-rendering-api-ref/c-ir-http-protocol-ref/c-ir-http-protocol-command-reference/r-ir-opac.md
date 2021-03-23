---
description: Opacità. Specifica l'opacità del materiale.
seo-description: Opacità. Specifica l'opacità del materiale.
seo-title: opaca
solution: Experience Manager
title: opaca
uuid: 0f5b11f0-af65-4abd-947e-7a28cb8de263
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

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

* Tinte solide e texture ripetibili applicate agli oggetti sovrapposti testurabili.
* Materiali di rivestimento per finestre applicati agli oggetti telaio di copertura per finestre.
* Decalli applicati a oggetti texture o a oggetti murali.

Se il materiale include un&#39;immagine con un canale alfa, `opac=` può essere utilizzato per rendere l&#39;immagine più trasparente, ma non più opaca.

## Proprietà {#section-352f7b82ede54159b6afb90ae4b559ec}

Attributo materiale. Ignorato se la selezione dell&#39;oggetto corrente o il materiale non supporta l&#39;opacità.

## Predefinito {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, per un materiale completamente opaco (se l&#39;immagine non include un canale alfa).
