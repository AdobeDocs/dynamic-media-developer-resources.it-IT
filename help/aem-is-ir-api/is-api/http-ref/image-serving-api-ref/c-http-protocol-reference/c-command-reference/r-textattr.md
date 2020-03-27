---
description: Attributi del livello di testo. Specifica attributi aggiuntivi per i livelli di testo che non sono disponibili come comandi rtf.
seo-description: Attributi del livello di testo. Specifica attributi aggiuntivi per i livelli di testo che non sono disponibili come comandi rtf.
seo-title: textAttr
solution: Experience Manager
title: textAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 07b3d263-2ed6-4363-83e1-3b841e9967c5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# textAttr{#textattr}

Attributi del livello di testo. Specifica attributi aggiuntivi per i livelli di testo che non sono disponibili come comandi rtf.

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span></span> </p> </td> 
  <td class="stentry"> <p>Consente di ridimensionare il livello di testo senza modificare le dimensioni dei font. Valori di risoluzione più elevati aumentano le dimensioni del testo renderizzato rispetto alle dimensioni del quadro; valori più piccoli riducono le dimensioni del testo. Risoluzione del testo in punti per pollice (in punti maggiore di 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> anti-aliasing </span></span> </p> </td> 
  <td class="stentry"> <p>Controlla la modalità di antialiasing utilizzata dal motore di rendering del testo. </p> <p> <span class="codeph"> off| Norma| croccante| sharp| forte| liscio </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> off </span> </p> </td> 
      <td class="stentry"> <p>Disattivate l’anti-alias del testo. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norma </span> </p> </td> 
      <td class="stentry"> <p>Attiva la modalità standard di anti-alias del testo (impostazione predefinita). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> croccante </span> </p> </td> 
      <td class="stentry"> <p>Selezionate la modalità di antialiasing di Photoshop <span class="codeph"> nitide </span> (solo <span class="codeph"> textPs= </span> ). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> sharp </span> </p> </td> 
      <td class="stentry"> <p>Selezionate <span class="codeph"> Nitidezza modalità anti-alias Photoshop </span> (solo <span class="codeph"> textPs= </span> ). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> Forte </span> </p> </td> 
      <td class="stentry"> <p>Selezionate la modalità di antialiasing <span class="codeph"> forte di Photoshop </span> (solo <span class="codeph"> textPs= </span> ). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>Controlla come viene utilizzata la risoluzione durante il rendering del testo </p> <p> <span class="codeph"> fixedRes| autoRes| maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>Utilizzare la risoluzione specificata. </p> <p>Utilizzate questa opzione se il testo deve essere rappresentato in una dimensione esatta rispetto al quadro di composizione. Se la casella di testo è troppo piccola, il testo potrebbe essere ritagliato in base alle dimensioni del livello (se specificato). Questa è l'unica opzione <span class="varname"> resMode </span> supportata da <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>Regolate automaticamente la risoluzione per riempire al meglio il rect del livello con il testo. </p> <p>Consente di regolare automaticamente le dimensioni del testo in modo che la casella di testo sia riempita il più possibile, senza rischi di troncamento. Se è attivata l’opzione di ritorno a capo automatico, il testo potrebbe essere reinserito nella risoluzione finale. <span class="varname"> res </span> viene ignorato se è selezionata l'opzione <span class="codeph"> AutoRes </span> . Non supportato da <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>utilizzare la risoluzione specificata; se necessario, riducetelo per evitare che il testo venga troncato sul bordo del livello. </p> <p>Utilizzate questa opzione per eseguire il rendering del testo alla risoluzione esatta specificata, a condizione che non si verifichi alcun ritaglio. In caso di ritaglio, la risoluzione viene automaticamente ridotta per assicurare che tutto il testo sia contenuto completamente all'interno della casella di testo. Se è attivata l’opzione di ritorno a capo automatico, il testo potrebbe essere reinserito nella risoluzione finale. Non supportato da <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Se la dimensione del livello di testo non viene specificata con size= o se viene specificata solo la larghezza, le impostazioni 'autoRes' e 'maxRes' vengono ignorate e la risoluzione specificata viene utilizzata per eseguire il rendering del testo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> word <span class="varname"> Wrap </span></span> </p> </td> 
  <td class="stentry"> <p>Specifica la modalità di wrapping. </p> <p> <span class="codeph"> involucro| noWrap| nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>Disattiva ritorno a capo automatico. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> involucro </span> </p> </td> 
      <td class="stentry"> <p>Abilita il ritorno a capo automatico standard. </p> <p>Se necessario, interrompe le parole lunghe. <span class="codeph"> textPs= </span> supporta solo <span class="codeph"> wrapper </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>Abilita ritorno a capo automatico senza interruzioni. </p> <p>Non spezza mai una parola, anche se alla fine viene troncata. Generalmente utilizzato in combinazione con <span class="codeph"> AutoRes </span> o <span class="codeph"> maxRes </span> per garantire che le parole lunghe non vengano mai interrotte. </p> </td> 
     </tr> 
    </table> </p> <p>Intorna <span class="codeph"> a capo </span> e <span class="codeph"> chiudi a capo </span> su bordi di parole e trattini. </p> </td> 
 </tr> 
</table>

## Proprietà {#section-114ca0b8585b403c873e2251478ad1d5}

Attributo del livello di testo. Ignorato dai livelli di immagine, colore in tinta unita e effetto. Si applica a `layer=0` se specificato per `layer=comp`.

## Predefinito {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Consultate anche {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
