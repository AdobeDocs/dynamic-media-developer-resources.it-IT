---
title: quantificare
description: Quantizzazione colore. Specifica gli attributi di quantizzazione del colore per la conversione dell'output GIF.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
TQID: 'https://experienceleague.adobe.com/m5e14tLMY1JAdZTzlw7iUZzXzL9yylP66MYi5XAeYtg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# quantificare{#quantize}

Quantizzazione colore. Specifica gli attributi di quantizzazione del colore per la conversione dell&#39;output GIF.

` quantize= *`tipo`*[, *`dithering`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> tipo </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> tipo di palette {adaptive|web|mac} </span> </p> <p>Selezionare ' <span class="codeph"> Web </span>' o ' <span class="codeph"> mac </span>' per scegliere una tavolozza predefinita oppure impostare su ' <span class="codeph"> adaptive </span>' per calcolare una tavolozza ottimale per l'immagine. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dithering </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> opzioni di retinatura </span> {diffuso|off} </p> <p>Selezionate 'diffonde' per la diffusione dell'errore Floyd-Steinberg o 'off' per disattivare il dithering. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>Numero di colori di output (numero intero) inclusi nella tavolozza adattiva </span> ' <span class="codeph">. </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> deve essere compreso tra 2 e 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>Elenco separato da virgole dei colori RGB forzati in formato esadecimale6. Consente di specificare i colori forzati da includere in una tavolozza </span> adattiva ' <span class="codeph">'. Se il numero di colori specificati è inferiore a <span class="codeph"> numColors </span>, verranno calcolati colori aggiuntivi in base al contenuto dell'immagine. </p> <p>Utilizzato solo se <span class="codeph"> fmt=gif </span> o <span class="codeph"> fmt=gif-alpha </span>. Altrimenti ignorato. I colori specificati con <span class="codeph"> <span class="varname"> colorList </span> </span> devono essere valori RGB in formato hex6 (vedere <span class="codeph"> color </span>). Non sono consentiti altri identificatori colore. </p> </td> 
 </tr> 
</table>

## Predefinito {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Esempio {#section-b3a979dc9ae3459baa093bf17310988f}

Generare una miniatura GIF utilizzando la tavolozza &#39; `web`&#39; e senza dithering:

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

Converti l’immagine in un GIF bicontonale con trasparenza dei colori chiave e forza i colori in bianco e nero:

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
