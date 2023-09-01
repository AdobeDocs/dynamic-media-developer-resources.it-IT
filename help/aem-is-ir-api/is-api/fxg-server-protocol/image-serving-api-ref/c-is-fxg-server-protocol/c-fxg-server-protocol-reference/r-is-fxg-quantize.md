---
title: quantificare
description: Quantizzazione colore. Specifica gli attributi di quantizzazione del colore per la conversione dell'output GIF.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---

# quantificare{#quantize}

Quantizzazione colore. Specifica gli attributi di quantizzazione del colore per la conversione dell&#39;output GIF.

` quantize= *`tipo`*[, *`dithering`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> tipo </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> tipo di palette </p> <p>Seleziona ' <span class="codeph"> web </span>' o ' <span class="codeph"> mac </span>' per scegliere una palette predefinita o impostata su ' <span class="codeph"> adattivo </span>' per calcolare una palette ottimale per l'immagine. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dithering </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuso|off} </span> opzioni dithering </p> <p>Selezionate 'diffonde' per la diffusione dell'errore Floyd-Steinberg o 'off' per disattivare il dithering. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>Numero di colori di output (numero intero) inclusi in ' <span class="codeph"> adattivo </span>tavolozza '. </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> deve essere compreso tra 2 e 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>Elenco separato da virgole dei colori RGB obbligatori in formato esadecimale6. Consente di specificare i colori forzati da includere in un' <span class="codeph"> adattivo </span>tavolozza '. Se il numero di colori specificato è minore di <span class="codeph"> numColors </span>, i colori aggiuntivi vengono calcolati in base al contenuto dell’immagine. </p> <p>Utilizzato solo se <span class="codeph"> fmt=gif </span> o <span class="codeph"> fmt=gif-alfa </span>. Altrimenti ignorato. I colori specificati con <span class="codeph"> <span class="varname"> colorList </span> </span> devono essere valori RGB in formato esadecimale6 (vedere <span class="codeph"> colore </span>); non sono consentiti altri specificatori di colore. </p> </td> 
 </tr> 
</table>

## Predefinito {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Esempio {#section-b3a979dc9ae3459baa093bf17310988f}

Genera una miniatura GIF utilizzando l’icona &quot; `web`&quot; e nessun dithering:

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

Converti l’immagine in GIF bicontonale con trasparenza dei colori chiave e forza i colori in bianco e nero:

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
