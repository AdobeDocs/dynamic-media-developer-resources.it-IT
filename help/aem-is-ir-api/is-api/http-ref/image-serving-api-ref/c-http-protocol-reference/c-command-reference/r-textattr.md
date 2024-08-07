---
title: textAttr
description: Attributi del livello di testo. Specifica attributi aggiuntivi per i livelli di testo che non sono disponibili come comandi rtf.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# textAttr{#textattr}

Attributi del livello di testo. Specifica attributi aggiuntivi per i livelli di testo che non sono disponibili come comandi rtf.

` textAttr= *`res`*[, *`antiAliasing`*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> risoluzione </span> </span> </p> </td> 
  <td class="stentry"> <p>Consente di ridimensionare il livello di testo senza modificare le dimensioni dei caratteri. I valori di risoluzione più elevati aumentano le dimensioni del testo di cui è stato eseguito il rendering rispetto alle dimensioni dell'area di lavoro, mentre i valori più piccoli riducono le dimensioni del testo. Risoluzione del testo in punti per pollice (int maggiore di 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> anti-alias </span> </span> </p> </td> 
  <td class="stentry"> <p>Controlla la modalità di anti-alias utilizzata dal motore di rendering del testo. </p> <p> <span class="codeph"> off | norma | nitido | acuto | forte | smussa </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> di </span> </p> </td> 
      <td class="stentry"> <p>Disattiva l'anti-alias del testo. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norma </span> </p> </td> 
      <td class="stentry"> <p>Attiva modalità anti-alias testo standard (impostazione predefinita). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> crisp </span> </p> </td> 
      <td class="stentry"> <p>Selezionare la modalità anti-alias di Photoshop <span class="codeph"> crisp </span> ( <span class="codeph"> textPs= </span> only). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> diesis </span> </p> </td> 
      <td class="stentry"> <p>Selezionare la modalità anti-alias di Photoshop <span class="codeph"> </span> (solo <span class="codeph"> textPs= </span>). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> </span> forte </p> </td> 
      <td class="stentry"> <p>Selezionare la modalità anti-alias di Photoshop <span class="codeph"> </span> (solo <span class="codeph"> textPs= </span>). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Controlla la modalità di utilizzo della risoluzione durante il rendering del testo </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>Utilizza la risoluzione specificata. </p> <p>Da utilizzare se il testo deve essere renderizzato con dimensioni esatte rispetto all’area di lavoro composta. Se la casella di testo è troppo piccola, è possibile che il testo venga ritagliato in base alle dimensioni del livello (se specificato). Questa è l'unica opzione <span class="varname"> resMode </span> supportata da <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>Regolate automaticamente la risoluzione per riempire al meglio il rettangolo del livello con il testo. </p> <p>Consente di regolare automaticamente le dimensioni del testo in modo che la casella di testo venga riempita il più possibile, senza rischio di troncamento. Se il ritorno a capo automatico è attivato, il testo può essere ridisposto alla risoluzione finale. La risoluzione <span class="varname"> </span> viene ignorata se si seleziona <span class="codeph"> autoRes </span>. Non supportato da <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>Utilizzate la risoluzione specificata; se necessario, riducetela per evitare che il testo venga troncato al rettangolo del livello. </p> <p>Consente di eseguire il rendering del testo alla risoluzione specificata, purché non si verifichi alcun ritaglio. In caso di ritaglio, la risoluzione viene automaticamente ridotta per garantire che tutto il testo sia contenuto completamente all'interno della casella di testo. Se il ritorno a capo automatico è attivato, il testo può essere ridisposto alla risoluzione finale. Non supportato da <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Se le dimensioni del livello di testo non sono specificate con size= o se è specificata solo la larghezza, le impostazioni "autoRes" e "maxRes" vengono ignorate. In questi casi, per il rendering del testo viene utilizzata la risoluzione specificata. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap </span> </span> </p> </td> 
  <td class="stentry"> <p>Specifica la modalità di wrapping. </p> <p> <span class="codeph"> a capo automatico | noWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>Disattiva word wrap. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> racchiude </span> </p> </td> 
      <td class="stentry"> <p>Attiva il ritorno a capo automatico standard. </p> <p>Rompe le parole lunghe, se necessario. <span class="codeph"> textPs= </span> supporta solo <span class="codeph"> wrapping </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>Attiva il ritorno a capo automatico unificatore. </p> <p>Non rompe mai una parola, anche se viene troncata alla fine. Utilizzato in genere con <span class="codeph"> autoRes </span> o <span class="codeph"> maxRes </span> per garantire che le parole lunghe non vengano mai interrotte. </p> </td> 
     </tr> 
    </table> </p> <p><span class="codeph"> applica a </span> e <span class="codeph"> il ritorno a capo automatico </span> sui limiti delle parole e i trattini. </p> </td> 
 </tr> 
</table>

## Proprietà {#section-114ca0b8585b403c873e2251478ad1d5}

Attributo livello testo. Ignorato dai livelli immagine, colore a tinta unita ed effetto. Si applica a `layer=0` se specificato per `layer=comp`.

## Predefinito {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Consultate anche {#section-68b0d2e2d0474e2097a9331ae272c224}

[testo=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [dimensione=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
