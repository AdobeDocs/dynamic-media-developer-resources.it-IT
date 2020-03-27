---
description: La vista principale è costituita dall’immagine con zoom.
seo-description: La vista principale è costituita dall’immagine con zoom.
seo-title: Visualizzazione zoom
solution: Experience Manager
title: Visualizzazione zoom
topic: Dynamic media
uuid: 34cb6c80-77eb-42b0-91dd-ae0369ea2881
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoom view{#zoom-view}

La vista principale è costituita dall’immagine con zoom.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;area di visualizzazione è controllato dal seguente selettore di classe CSS:

```
.s7zoomviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo nel formato esadecimale della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>Cursore visualizzato sulla vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la vista principale.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Sui sistemi desktop il componente supporta il selettore `cursortype` di attributi che può essere applicato alla `.s7zoomview` classe. Controlla il tipo di cursore in base allo stato del componente e all’azione dell’utente. The following `cursortype` values are supported:

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

