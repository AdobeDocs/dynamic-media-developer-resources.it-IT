---
title: PageView.iconEffect
description: PageView.iconEffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: cdd96e58-d805-47d6-bf26-9ebd90afd535
TQID: 'https://experienceleague.adobe.com/BChSE62IgfhsabTf1I-XlAJLqvRhai4U48vNEg-MkQ4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# PageView.iconEffect{#pageview-iconeffect}

` [PageView.|<containerId>_pageView.]iconeffect=0|1[, *`conteggio`*][, *`dissolvenza`*][, *`autoHide`*]`

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Consente la visualizzazione dell'effetto iconeffect <span class="codeph"></span> nella parte superiore dell'immagine quando quest'ultima è in stato di reimpostazione e suggerisce un'azione disponibile per interagire con l'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> conteggio</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte che l'iconeffect <span class="codeph"></span> viene visualizzato e rivisualizzato. Il valore <span class="codeph"> -1</span> indica che l'icona viene sempre visualizzata indefinitamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dissolvenza <span class="codeph"><span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata dell'animazione mostra/nascondi, in secondi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Nascondi automaticamente</span></span> </p> </td> 
   <td colname="col2"> <p>Imposta il numero di secondi in cui l'effetto iconeffect</span> di <span class="codeph"> rimane completamente visibile prima che venga nascosto automaticamente. Ossia, il tempo dopo il completamento dell'animazione di dissolvenza in entrata, ma prima dell'inizio dell'animazione di dissolvenza in uscita. L'impostazione <span class="codeph"> 0</span> disattiva il comportamento Nascondi automatico. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-b6e5e52698d4492f9d6350e7e312bb1b}

Facoltativo.

## Predefinito {#section-7d0fc8fa09b34c288ed32ef7faa84604}

`1,1,0.3,3`

## Esempio {#section-95db1bfcccf241089654363203b19977}

`iconeffect=0`
