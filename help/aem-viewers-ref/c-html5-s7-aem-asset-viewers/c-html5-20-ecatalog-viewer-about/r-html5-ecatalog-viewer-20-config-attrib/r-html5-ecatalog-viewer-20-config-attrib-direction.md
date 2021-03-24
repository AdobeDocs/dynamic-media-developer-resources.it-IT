---
description: direzione
solution: Experience Manager
title: direzione
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 3%

---


# direzione{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|sinistra|destra  </span> </p> </td> 
   <td colname="col2"> <p>Specifica il modo in cui le pagine vengono visualizzate nella visualizzazione principale e nelle miniature. Specifica anche il modo in cui l’utente interagisce con l’interfaccia utente del visualizzatore per cambiare tra i fotogrammi del catalogo. </p> <p>Quando si utilizza <span class="codeph"> sinistra </span>, imposta l'allineamento a destra per la pagina iniziale e a sinistra per l'ultima pagina. Unisce le singole immagini secondarie di pagina per l’ordine di rendering da sinistra a destra. Imposta anche la visualizzazione principale per utilizzare l'animazione diapositiva da destra a sinistra per far avanzare il catalogo (nel caso in cui <span class="codeph"> PageView.frametransition </span> sia impostato su slide). Infine, le miniature sono impostate per l’ordine di riempimento da sinistra a destra. </p> <p>Allo stesso modo, quando si utilizza <span class="codeph"> destra </span> imposta l'allineamento a sinistra per la pagina iniziale e a destra per l'ultima pagina. Unisce le singole immagini secondarie di pagina per l’ordine di rendering da destra a sinistra. Imposta anche la visualizzazione principale per utilizzare l'animazione diapositiva da sinistra a destra per far avanzare il catalogo (nel caso in cui <span class="codeph"> PageView.frametransition </span> sia impostato su slide). Infine, inverte l’ordine delle miniature in modo che la visualizzazione delle miniature sia riempita in direzione da destra a sinistra e dall’alto verso il basso. </p> <p>Quando è impostato <span class="codeph"> auto </span>, il visualizzatore applica la modalità <span class="codeph"> right </span> quando le impostazioni internazionali sono impostate su <span class="codeph"> ja; </span>in caso contrario, utilizza la modalità <span class="codeph"> sinistra </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-a66ce10d6c0b449883f654e7e0657e2c}

Facoltativo.

## Predefinito {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## Esempio {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
