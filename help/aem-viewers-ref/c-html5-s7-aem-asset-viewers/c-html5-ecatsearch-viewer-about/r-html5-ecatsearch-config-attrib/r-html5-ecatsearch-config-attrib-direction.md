---
title: direzione
description: direzione
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---

# direzione{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>Specifica il modo in cui le pagine vengono visualizzate nella visualizzazione principale e nelle miniature. Specifica inoltre il modo in cui l’utente interagisce con l’interfaccia utente del visualizzatore per passare da una cornice di catalogo all’altra. </p> <p>Quando <span class="codeph"> left </span> viene utilizzato per impostare un allineamento a destra per la pagina iniziale e un allineamento a sinistra per l'ultima pagina. Unisce le singole immagini secondarie della pagina per l’ordine di rendering da sinistra a destra. Inoltre, imposta la vista principale in modo che utilizzi l'animazione di scorrimento da destra a sinistra per far avanzare il catalogo (nel caso in cui <span class="codeph"> PageView.frametransition </span> è impostato su slide). Infine, le miniature vengono impostate per un ordine di visualizzazione da sinistra a destra. </p> <p>Analogamente, quando <span class="codeph"> destra </span> viene utilizzato per impostare un allineamento a sinistra per la pagina iniziale e un allineamento a destra per l'ultima pagina. Unisce le singole immagini secondarie della pagina per l’ordine di rendering da destra a sinistra. Inoltre, imposta la vista principale in modo che utilizzi l'animazione di scorrimento da sinistra a destra per far avanzare il catalogo (nel caso in cui <span class="codeph"> PageView.frametransition </span> è impostato su slide). Infine, inverte l’ordine delle miniature in modo che la vista delle miniature sia riempita da destra a sinistra e dall’alto al basso. </p> <p>Quando <span class="codeph"> auto </span> è impostato, il visualizzatore applica <span class="codeph"> destra </span> modalità quando la lingua è impostata su <span class="codeph"> ja; </span>in caso contrario utilizza <span class="codeph"> left </span> modalità. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-a66ce10d6c0b449883f654e7e0657e2c}

Facoltativo.

## Predefinito {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Esempio {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
