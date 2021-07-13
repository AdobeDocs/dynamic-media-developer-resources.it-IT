---
description: La vista principale è costituita dall’immagine zoomabile.
solution: Experience Manager
title: Visualizzazione zoom
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Zoom
role: Developer,User
exl-id: 286b9df4-88db-4e5d-aab4-9cbe01195e57
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# Visualizzazione zoom{#zoom-view}

La vista principale è costituita dall’immagine zoomabile.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato con il seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo nel formato esadecimale della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursore  </span> </p> </td> 
   <td colname="col2"> <p>Il cursore viene visualizzato sulla vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio : per rendere trasparente la visualizzazione principale.

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Nei sistemi desktop il componente supporta il selettore di attributi `cursortype` che può essere applicato alla classe `.s7zoomview` e controlla il tipo di cursore in base allo stato del componente e all’azione dell’utente. Sono supportati i seguenti valori `cursortype`:

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valore </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default  </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando l'immagine non è zoomabile a causa di una piccola risoluzione dell'immagine, delle impostazioni dei componenti o di entrambe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomina  </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando l'immagine può essere ingrandita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset  </span> </p> </td> 
   <td colname="col2"> <p>Visualizzata quando l'immagine è al livello di zoom massimo e può essere ripristinata al suo stato iniziale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trascinare  </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando un utente fa scorrere l'immagine con lo stato di zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>
