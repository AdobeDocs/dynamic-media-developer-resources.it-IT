---
description: Opacità. Specifica l’opacità del materiale.
seo-description: Opacità. Specifica l’opacità del materiale.
seo-title: opac
solution: Experience Manager
title: opac
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f5b11f0-af65-4abd-947e-7a28cb8de263
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# opac{#opac}

Opacità. Specifica l’opacità del materiale.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Opacità materiale (percentuale); 0...100 </p> </td> 
 </tr> 
</table>

Le seguenti combinazioni di materiale/oggetto supportano l’opacità variabile:

* Tinte piatte e texture ripetibili applicate agli oggetti sovrapposti con texture.
* Materiali di rivestimento di finestre applicati agli oggetti telaio di copertura della finestra.
* Decorazioni applicate a oggetti strutturabili o a oggetti murali.

Se il materiale include un&#39;immagine con un canale alfa, è possibile utilizzare `opac=` per rendere l&#39;immagine più trasparente, ma non più opaca.

## Proprietà {#section-352f7b82ede54159b6afb90ae4b559ec}

Attributo materiale. Ignorato se la selezione dell&#39;oggetto corrente o il materiale non supporta l&#39;opacità.

## Predefinito {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, per un materiale completamente opaco (se l&#39;immagine non include un canale alfa).
