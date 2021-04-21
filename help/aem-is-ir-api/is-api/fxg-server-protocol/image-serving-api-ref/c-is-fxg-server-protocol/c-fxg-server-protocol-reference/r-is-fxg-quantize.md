---
description: quantizzazione del colore. Specifica gli attributi di quantizzazione del colore per la conversione dell'output GIF.
solution: Experience Manager
title: quantificare
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 1%

---


# quantizzare{#quantize}

quantizzazione del colore. Specifica gli attributi di quantizzazione del colore per la conversione dell&#39;output GIF.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Tipo di  </span> palette {adaptive|web|mac} </p> <p>Seleziona ' <span class="codeph"> web </span>' o ' <span class="codeph"> mac </span>' per scegliere una palette predefinita oppure imposta su ' <span class="codeph"> adattivo </span>' per calcolare una palette ottimale per l'immagine. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dietesi  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Opzioni di  </span> dithering di {diffusa|off} </p> <p>Selezionare 'diffusa' per la diffusione dell'errore Floyd-Steinberg o 'off' per disabilitare il dithering. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>Numero di colori di output (numero intero) inclusi nella palette ' <span class="codeph"> adattiva </span>'. </p> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> deve essere compreso tra 2 e 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>Elenco dei colori RGB forzati separati da virgole in formato esadecimale6. Consente di specificare i colori forzati da includere in una palette ' <span class="codeph"> adattiva </span>'. Se il numero di colori specificato è inferiore a <span class="codeph"> numColors </span>, vengono calcolati colori aggiuntivi in base al contenuto dell'immagine. </p> <p>Utilizzato solo se <span class="codeph"> fmt=gif </span> o <span class="codeph"> fmt=gif-alpha </span>. Ignorato altrimenti. I colori specificati con <span class="codeph"> <span class="varname"> colorList </span> </span> devono essere valori RGB in formato esadecimale6 (vedere <span class="codeph"> colore </span>); non sono consentiti altri identificatori di colore. </p> </td> 
 </tr> 
</table>

## Predefinito {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Esempio {#section-b3a979dc9ae3459baa093bf17310988f}

Genera una miniatura GIF utilizzando la palette `web` senza dithering:

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

Converti l&#39;immagine in GIF bictonale con trasparenza a colori chiave e forza i colori in bianco e nero:

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
