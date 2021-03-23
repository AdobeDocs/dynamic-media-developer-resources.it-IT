---
description: quantizzazione del colore. Specifica gli attributi di quantizzazione del colore per la conversione dell'output GIF.
seo-description: quantizzazione del colore. Specifica gli attributi di quantizzazione del colore per la conversione dell'output GIF.
seo-title: quantificare
solution: Experience Manager
title: quantificare
uuid: 624cdc45-51f2-4b18-a658-311770974521
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

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
