---
description: La vista principale è costituita dall’immagine con zoom.
seo-description: La vista principale è costituita dall’immagine con zoom.
seo-title: Visualizzazione zoom
solution: Experience Manager
title: Visualizzazione zoom
topic: Dynamic media
uuid: 06464e36-8c9c-4d3c-b4e5-5911f002568c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoom view{#zoom-view}

La vista principale è costituita dall’immagine con zoom.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;area di visualizzazione è controllato dal seguente selettore di classe CSS:

```
.s7basiczoomviewer .s7zoomview
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
   <td colname="col2"> <p>Il cursore viene visualizzato sulla vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la vista principale.

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Sui sistemi desktop il componente supporta il selettore `cursortype` di attributi che può essere applicato alla `.s7zoomview` classe e controlla il tipo di cursore in base allo stato del componente e all’azione dell’utente. The following `cursortype` values are supported:

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valore </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando l’immagine non può essere ingrandita a causa di una piccola risoluzione dell’immagine, delle impostazioni del componente o di entrambi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomina </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando è possibile ingrandire l’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>Visualizzata quando l’immagine è al livello di zoom massimo e può essere reimpostata allo stato iniziale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> drag </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando un utente esegue il panning dell'immagine con lo stato di zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

