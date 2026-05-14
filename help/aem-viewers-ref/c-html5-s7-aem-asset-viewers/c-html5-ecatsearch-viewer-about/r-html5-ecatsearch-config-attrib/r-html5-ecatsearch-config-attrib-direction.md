---
title: direzione
description: direzione
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
TQID: 'https://experienceleague.adobe.com/tNKu0P8Sgoxas-opiWd1GWkuWYWDfXE0-j1A-p-j-jM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 206
ht-degree: 1%

---

# direzione{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|sinistra|destra </span> </p> </td> 
   <td colname="col2"> <p>Specifica il modo in cui le pagine vengono visualizzate nella visualizzazione principale e nelle miniature. Specifica inoltre il modo in cui l’utente interagisce con l’interfaccia utente del visualizzatore per passare da una cornice di catalogo all’altra. </p> <p>Quando si utilizza <span class="codeph"> left </span>, imposta l'allineamento a destra per la pagina iniziale e a sinistra per l'ultima pagina. Unisce le singole immagini secondarie della pagina per l’ordine di rendering da sinistra a destra. Inoltre, imposta la visualizzazione principale in modo che utilizzi l'animazione di scorrimento da destra a sinistra per far avanzare il catalogo (nel caso in cui <span class="codeph"> PageView.frametransition </span> sia impostato su slide). Infine, le miniature vengono impostate per un ordine di visualizzazione da sinistra a destra. </p> <p>Analogamente, quando si utilizza <span class="codeph"> </span> destro, imposta un allineamento a sinistra per la pagina iniziale e un allineamento a destra per l'ultima pagina. Unisce le singole immagini secondarie della pagina per l’ordine di rendering da destra a sinistra. Inoltre, imposta la visualizzazione principale in modo che utilizzi l'animazione di scorrimento da sinistra a destra per far avanzare il catalogo (nel caso in cui <span class="codeph"> PageView.frametransition </span> sia impostato su slide). Infine, inverte l’ordine delle miniature in modo che la vista delle miniature sia riempita da destra a sinistra e dall’alto al basso. </p> <p>Quando è impostata l'opzione <span class="codeph"> auto </span>, il visualizzatore applica la modalità <span class="codeph"> right </span> quando le impostazioni locali sono impostate su <span class="codeph"> ja; </span>altrimenti, utilizza la modalità <span class="codeph"> left </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-a66ce10d6c0b449883f654e7e0657e2c}

Facoltativo.

## Predefinito {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Esempio {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
