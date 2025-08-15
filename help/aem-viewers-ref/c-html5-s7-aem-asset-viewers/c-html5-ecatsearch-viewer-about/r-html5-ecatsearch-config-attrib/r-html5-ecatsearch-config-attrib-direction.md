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
   <td colname="col2"> <p>Specifica il modo in cui le pagine vengono visualizzate nella visualizzazione principale e le miniature. Specifica inoltre il modo in cui il utente interagisce con l'interfaccia del utente visualizzatore per passare da un frame di catalogo all'altro. </p> <p>Quando <span class="codeph"> si utilizza sinistra </span> viene impostato un allineamento a destra per la pagina iniziale e un allineamento a sinistra per l'ultima pagina. Cuce le singole immagini secondarie delle pagine per l'ordine di rendering da sinistra a destra. Imposta inoltre la visualizzazione principale in modo che utilizzi l'animazione diapositiva da destra a sinistra per far avanzare il catalogo (nel caso in cui <span class="codeph"> PageView.frametransition </span> sia impostato su diapositiva). Infine, le miniature vengono impostate per un ordine di riempimento da sinistra a destra. </p> <p>Analogamente, quando <span class="codeph"> si utilizza l'opzione destra </span> , viene impostato un allineamento a sinistra per la pagina iniziale e un allineamento a destra per l'ultima pagina. Cuce le singole immagini secondarie di pagina per un ordine di rendering da destra a sinistra. Imposta inoltre la visualizzazione principale in modo che utilizzi l'animazione diapositiva da sinistra a destra per far avanzare il catalogo (nel caso in cui <span class="codeph"> PageView.frametransition </span> sia impostato su diapositiva). Infine, inverte l'ordine delle miniature in modo che la visualizzazione delle miniature venga riempita nella direzione da destra a sinistra, dall'alto verso il basso. </p> <p>Quando <span class="codeph"> auto </span> è impostato, il visualizzatore applica <span class="codeph"> la modalità destra </span> quando la lingua è impostata su <span class="codeph"> ja; </span>In caso contrario, utilizza la <span class="codeph"> modalità sinistra </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-a66ce10d6c0b449883f654e7e0657e2c}

Facoltativo.

## Predefinito {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Esempio {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
