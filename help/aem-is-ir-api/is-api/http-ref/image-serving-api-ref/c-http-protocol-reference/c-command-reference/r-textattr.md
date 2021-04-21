---
description: Attributi del livello di testo. Specifica gli attributi aggiuntivi per i livelli di testo che non sono disponibili come comandi rtf.
solution: Experience Manager
title: textAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 1%

---


# textAttr{#textattr}

Attributi del livello di testo. Specifica gli attributi aggiuntivi per i livelli di testo che non sono disponibili come comandi rtf.

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res  </span> </span> </p> </td> 
  <td class="stentry"> <p>Consente di ridimensionare il livello di testo senza modificare le dimensioni dei font. Valori di risoluzione più elevati aumentano le dimensioni del testo renderizzato rispetto alle dimensioni dell'area di lavoro; valori più piccoli riducono le dimensioni del testo. Risoluzione del testo in punti per pollice (in numero maggiore di 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> anti-aliasing  </span> </span> </p> </td> 
  <td class="stentry"> <p>Controlla la modalità anti-aliasing utilizzata dal motore di rendering del testo. </p> <p> <span class="codeph"> off | norma | croccante | diesis | forte | liscio  </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> off  </span> </p> </td> 
      <td class="stentry"> <p>Disattiva l'anti-aliasing del testo. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norma  </span> </p> </td> 
      <td class="stentry"> <p>Attiva la modalità standard di anti-aliasing del testo (impostazione predefinita). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> croccante  </span> </p> </td> 
      <td class="stentry"> <p>Seleziona la modalità anti-aliasing Photoshop <span class="codeph"> croccante </span> ( <span class="codeph"> textPs= </span> solo). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> acuto  </span> </p> </td> 
      <td class="stentry"> <p>Seleziona la modalità anti-aliasing Photoshop <span class="codeph"> affilato </span> ( <span class="codeph"> textPs= </span> solo). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> Forte </span> </p> </td> 
      <td class="stentry"> <p>Seleziona la modalità anti-aliasing Photoshop <span class="codeph"> strong </span> ( <span class="codeph"> textPs= </span> solo). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Controlla come viene utilizzata la risoluzione durante il rendering del testo </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes  </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes  </span> </p> </td> 
      <td class="stentry"> <p>Utilizzare la risoluzione specificata. </p> <p>Utilizzate questa opzione per eseguire il rendering del testo in una dimensione esatta rispetto al quadro di composizione. Se la casella di testo è troppo piccola, il testo può essere ritagliato in base alle dimensioni del livello (se specificato). Questa è l'unica opzione <span class="varname"> resMode </span> supportata da <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes  </span> </p> </td> 
      <td class="stentry"> <p>Regolare automaticamente la risoluzione per riempire al meglio la correzione del livello con il testo. </p> <p>Consente di regolare automaticamente le dimensioni del testo in modo che la casella di testo venga riempita il più possibile, senza rischio di troncamento. Se è abilitato il ritorno a capo automatico, il testo può essere ritoccato alla risoluzione finale. <span class="varname"> res  </span> viene ignorato se  <span class="codeph"> autoRes  </span> è selezionato. Non supportato da <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes  </span> </p> </td> 
      <td class="stentry"> <p>utilizzare la risoluzione specificata; se necessario, riducetelo per evitare che il testo venga troncato sul bordo del livello. </p> <p>Utilizzare per eseguire il rendering del testo alla risoluzione esatta specificata, purché non si verifichi alcun ritaglio. In caso di ritaglio, la risoluzione viene automaticamente ridotta per garantire che tutto il testo sia contenuto completamente all’interno della casella di testo. Se è abilitato il ritorno a capo automatico, il testo può essere ritoccato alla risoluzione finale. Non supportato da <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Se la dimensione del livello di testo non viene specificata con size= o se viene specificata solo la larghezza, le impostazioni 'autoRes' e 'maxRes' vengono ignorate e la risoluzione specificata viene utilizzata per eseguire il rendering del testo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap  </span> </span> </p> </td> 
  <td class="stentry"> <p>Specifica la modalità di wrapping. </p> <p> <span class="codeph"> avvolgere | noWrap | nbWrap  </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap  </span> </p> </td> 
      <td class="stentry"> <p>Disattiva il ritorno a capo automatico. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> avvolgere  </span> </p> </td> 
      <td class="stentry"> <p>Attiva il ritorno a capo automatico standard. </p> <p>Se necessario, interrompe le parole lunghe. <span class="codeph"> textPs= supporta  </span> solo il  <span class="codeph"> ritorno a capo  </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap  </span> </p> </td> 
      <td class="stentry"> <p>Attiva ritorno a capo automatico senza interruzioni. </p> <p>Non rompe mai una parola, anche se alla fine viene troncata. Generalmente utilizzato in combinazione con <span class="codeph"> autoRes </span> o <span class="codeph"> maxRes </span> per garantire che le parole lunghe non vengano mai interrotte. </p> </td> 
     </tr> 
    </table> </p> <p>Inclusione automatica di <span class="codeph"> e </span> nbwrapping </span> su bordi e trattini delle parole.<span class="codeph"> </span></p> </td> 
 </tr> 
</table>

## Proprietà {#section-114ca0b8585b403c873e2251478ad1d5}

Attributo livello testo. Ignorato dai livelli immagine, colore solido e effetto. Si applica a `layer=0` se specificato per `layer=comp`.

## Predefinito {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Consultate anche {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
