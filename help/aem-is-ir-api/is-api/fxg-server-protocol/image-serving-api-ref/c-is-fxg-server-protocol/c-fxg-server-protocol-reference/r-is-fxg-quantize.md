---
description: Quantizzazione del colore. Specifica gli attributi di quantizzazione del colore per la conversione dell’output in formato GIF.
seo-description: Quantizzazione del colore. Specifica gli attributi di quantizzazione del colore per la conversione dell’output in formato GIF.
seo-title: quantificare
solution: Experience Manager
title: quantificare
topic: Scene7 Image Serving - Image Rendering API
uuid: 624cdc45-51f2-4b18-a658-311770974521
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# quantizzare{#quantize}

Quantizzazione del colore. Specifica gli attributi di quantizzazione del colore per la conversione dell’output in formato GIF.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adattivo|web|mac}, tipo di  </span> palette </p> <p>Selezionare ' <span class="codeph"> web </span>' o ' <span class="codeph"> mac </span>' per scegliere una palette predefinita, oppure impostare ' <span class="codeph"> adattivo </span>' per calcolare una palette ottimale per l'immagine. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dithering  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Opzioni di  </span> dithering di {diffusa|disattivata} </p> <p>Selezionare 'diffondere' per la diffusione di errori Floyd-Steinberg o 'off' per disabilitare il dithering. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>Numero di colori di output (numero intero) inclusi nella palette ' <span class="codeph"> adattiva </span>'. </p> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> deve essere compreso tra 2 e 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>Elenco separato da virgole di colori RGB forzati in formato ex6. Consente di specificare i colori forzati da includere in una palette ' <span class="codeph"> adattiva </span>'. Se il numero di colori specificato è inferiore a <span class="codeph"> numColors </span>, vengono calcolati colori aggiuntivi in base al contenuto dell'immagine. </p> <p>Utilizzata solo se <span class="codeph"> fmt=gif </span> o <span class="codeph"> fmt=gif-alpha </span>. Ignorato in caso contrario. I colori specificati con <span class="codeph"> <span class="varname"> colorList </span> </span> devono essere valori RGB in formato hex6 (vedere <span class="codeph"> color </span>); non sono consentiti altri identificatori di colore. </p> </td> 
 </tr> 
</table>

## Predefinito {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Esempio {#section-b3a979dc9ae3459baa093bf17310988f}

Generare una miniatura GIF utilizzando la palette &#39; `web`&#39; senza dithering:

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

Convertite l’immagine in un GIF biconale con trasparenza a colori chiave e forzate i colori in bianco e nero:

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
