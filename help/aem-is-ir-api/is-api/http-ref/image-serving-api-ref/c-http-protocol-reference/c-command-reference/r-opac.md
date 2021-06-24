---
description: Regolare l'opacità dell'immagine. Consente di ridurre l’opacità in primo piano di un livello immagine, testo, colore solido o effetto.
solution: Experience Manager
title: opaca
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---

# opaca{#opac}

Regolare l&#39;opacità dell&#39;immagine. Consente di ridurre l’opacità in primo piano di un livello immagine, testo, colore solido o effetto.

`opac= *``*[, *`opacityfillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> opacità</span> </p> </td> 
  <td class="stentry"> <p>opacità primaria (0...100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>opacità di riempimento (0...100 int). </p></td> 
 </tr> 
</table>

L&#39;opacità in primo piano di un livello immagine è determinata dalla maschera di livello o dal canale alfa dell&#39;immagine oppure, se non sono presenti, è del 100%. L&#39;opacità in primo piano di un livello di testo è del 100% e quella di un livello di colore solido è impostata da `color=`.

`opac=` non modifica mai l&#39;opacità delle aree riempite con  `color=` o  `bgColor=`, ad eccezione delle aree in primo piano dei livelli di colore solido ed effetto (impostati con  `color=`).

Se specificato in un livello di immagine, testo o colore solido, *`opacity`* applica l&#39;intero livello, inclusi tutti i livelli di effetto associati, mentre *`fillOpacity`* si applica solo al contenuto del livello principale. Se specificato in un livello di effetto, *`opacity`* viene applicato al livello di effetto, mentre *`fillOpacity`* viene ignorato.

L&#39;opacità effettiva per il contenuto del livello principale è ( *`opacity`* * *`fillOpacity`* / 100). L&#39;opacità effettiva per i livelli di effetto è (principale *`opacity`* * effetto *`opacity`* / 100).

## Proprietà {#section-ac3f136ff1584a2eab87500b7164f7fa}

Attributo livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`.

## Predefinito {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, per nessuna modifica nell&#39;opacità del livello.

## Esempio {#section-9710810e96af40538652e8ae4aadd3be}

... `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`...

L&#39;opacità del testo in questo esempio è 90*70/100=63% e l&#39;opacità del livello di effetto è 90*50/100=45%.

## Consultate anche {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
