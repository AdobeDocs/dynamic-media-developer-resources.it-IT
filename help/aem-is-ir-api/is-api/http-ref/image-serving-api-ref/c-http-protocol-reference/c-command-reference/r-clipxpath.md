---
description: Percorso clip livello invertito. Specifica un percorso di clip di esclusione per il livello corrente. Tutte le parti del livello che si trovano all'interno dell'area definita da clipXPath= sono rese trasparenti.
solution: Experience Manager
title: clipXPath
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---

# clipXPath{#clipxpath}

Percorso clip livello invertito. Specifica un percorso di clip di esclusione per il livello corrente. Tutte le parti del livello che si trovano all&#39;interno dell&#39;area definita da clipXPath= sono rese trasparenti.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Dati del percorso. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>Nome del percorso incorporato nell’immagine sorgente del livello (solo ASCII). </p></td> 
 </tr> 
</table>

Per ulteriori informazioni, consultate [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) , inclusa una descrizione di `*`pathName`*` e `*`pathDefinition`*`.

## Proprietà {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Attributo livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato se `clipPath=` non è specificato. Ignorato dai livelli di effetto.

## Predefinito {#section-d1986aa31af14767aeb1b4a57add67f4}

Nessuno.

## Consultate anche {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
