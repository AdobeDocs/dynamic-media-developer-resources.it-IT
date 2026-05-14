---
title: clipXPath
description: Percorso clip livello invertito. Specifica un tracciato clip di esclusione per il livello corrente. Tutte le parti del livello che si trovano all'interno dell'area definita da clipXPath= vengono rese trasparenti.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
TQID: 'https://experienceleague.adobe.com/G8pumLDbSj2TX80gqSTw-Bu4HxlRn92gyFpETIImBWw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 2%

---

# clipXPath{#clipxpath}

Percorso clip livello invertito. Specifica un tracciato clip di esclusione per il livello corrente. Tutte le parti del livello che si trovano all&#39;interno dell&#39;area definita da clipXPath= vengono rese trasparenti.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *`nomePercorso`*&#42;[, *`nomePercorso`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> definizione percorso</span> </span> </p> </td> 
  <td class="stentry"> <p>Dati percorso. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nomePercorso</span> </span> </p> </td> 
  <td class="stentry"> <p>Nome del percorso incorporato nell'immagine sorgente del livello (solo ASCII). </p></td> 
 </tr> 
</table>

Vedere [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) per ulteriori informazioni, inclusa una descrizione di `*`pathName`*` e `*`pathDefinition`*`.

## Proprietà {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Attributo livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato se `clipPath=` non è specificato. Ignorato dai livelli degli effetti.

## Predefinito {#section-d1986aa31af14767aeb1b4a57add67f4}

Nessuno.

## Consultate anche {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
