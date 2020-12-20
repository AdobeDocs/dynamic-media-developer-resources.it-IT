---
description: Tracciato Clip Livello Invertito. Specifica un percorso di clip di esclusione per il livello corrente. Tutte le parti del livello che si trovano all’interno dell’area definita da clipXPath= vengono sottoposte a rendering trasparente.
seo-description: Tracciato Clip Livello Invertito. Specifica un percorso di clip di esclusione per il livello corrente. Tutte le parti del livello che si trovano all’interno dell’area definita da clipXPath= vengono sottoposte a rendering trasparente.
seo-title: clipXPath
solution: Experience Manager
title: clipXPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a4062f3f-5dba-4514-acde-e1b7d608a2e9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 3%

---


# clipXPath{#clipxpath}

Tracciato Clip Livello Invertito. Specifica un percorso di clip di esclusione per il livello corrente. Tutte le parti del livello che si trovano all’interno dell’area definita da clipXPath= vengono sottoposte a rendering trasparente.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *`pathNamepathName `*&#42;[, *``*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Dati percorso. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>Nome del tracciato incorporato nell’immagine sorgente del livello (solo ASCII). </p></td> 
 </tr> 
</table>

Per ulteriori informazioni, vedere [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), inclusa una descrizione di ` *`pathName`*` e ` *`pathDefinition`*`.

## Proprietà {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Attributo layer. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato se `clipPath=` non è specificato. Ignorato dai livelli degli effetti.

## Predefinito {#section-d1986aa31af14767aeb1b4a57add67f4}

Nessuno.

## Consultate anche {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
