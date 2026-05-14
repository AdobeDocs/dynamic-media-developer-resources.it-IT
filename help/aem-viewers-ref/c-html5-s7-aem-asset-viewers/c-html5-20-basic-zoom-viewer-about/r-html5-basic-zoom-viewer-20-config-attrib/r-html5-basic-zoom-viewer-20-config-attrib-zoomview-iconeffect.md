---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: faec00b3-b981-4831-bc97-dff442389133
TQID: 'https://experienceleague.adobe.com/pVlxftuVZ3kgRfQElIXwGcoTgjWduRisjcBZGKq85LE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`conteggio`*][, *`dissolvenza`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Consente la visualizzazione di IconEffect nella parte superiore dell'immagine quando questa è in stato di ripristino e suggerisce un'azione disponibile per interagire con l'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> conteggio</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte che IconEffect viene visualizzato e rivisualizzato. Il valore <span class="codeph"> -1</span> indica che l'icona viene sempre visualizzata indefinitamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dissolvenza <span class="codeph"> <span class="varname"></span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata dell'animazione mostra/nascondi, in secondi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p>Imposta il numero di secondi in cui IconEffect rimane completamente visibile prima che venga nascosto automaticamente. Ossia, il tempo dopo il completamento dell'animazione di dissolvenza in entrata, ma prima dell'inizio dell'animazione di dissolvenza in uscita. L'impostazione <span class="codeph"> 0</span> disattiva il comportamento Nascondi automatico. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-50bcd15223174bb79ce08b31ea03d682}

Facoltativo.

## Predefinito {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## Esempio {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`
