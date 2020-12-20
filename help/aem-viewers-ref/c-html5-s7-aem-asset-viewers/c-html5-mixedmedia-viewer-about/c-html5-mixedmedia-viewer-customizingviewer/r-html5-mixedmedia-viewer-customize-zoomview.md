---
description: In modalità zoom continuo, la vista principale consiste nell’immagine con zoom quando la risorsa corrente è una singola immagine.
seo-description: In modalità zoom continuo, la vista principale consiste nell’immagine con zoom quando la risorsa corrente è una singola immagine.
seo-title: Visualizzazione zoom
solution: Experience Manager
title: Visualizzazione zoom
topic: Dynamic media
uuid: c9113275-eec6-4014-b7ad-3ae9f2cf01d9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---


# Visualizzazione zoom{#zoom-view}

In modalità zoom continuo, la vista principale consiste nell’immagine con zoom quando la risorsa corrente è una singola immagine.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;area di visualizzazione è controllato dal seguente selettore di classe CSS:

```
.s7mixedmediaviewer .s7zoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo nel formato esadecimale della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>Cursore visualizzato sulla vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la visualizzazione zoom.

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

Sui sistemi desktop il componente supporta il selettore di attributi `cursortype` che può essere applicato alla classe `.s7zoomview`. Controlla il tipo di cursore in base allo stato del componente e all’azione dell’utente. Sono supportati i seguenti valori `cursortype`:

* `default`

   Visualizzato quando l’immagine non può essere ingrandita a causa di una piccola risoluzione dell’immagine, delle impostazioni del componente o di entrambi.

* `zoomin`

   Visualizzato quando è possibile ingrandire l’immagine.

* `reset`

   Visualizzata quando l’immagine è al livello di zoom massimo e può essere reimpostata allo stato iniziale.

* `drag`

   Visualizzato quando l’utente esegue il panning dell’immagine con lo stato di zoom.

* `slide`

   Visualizzato quando l’utente esegue lo scambio di immagini eseguendo un passaggio del dito o un gesto di scorrimento orizzontale.

