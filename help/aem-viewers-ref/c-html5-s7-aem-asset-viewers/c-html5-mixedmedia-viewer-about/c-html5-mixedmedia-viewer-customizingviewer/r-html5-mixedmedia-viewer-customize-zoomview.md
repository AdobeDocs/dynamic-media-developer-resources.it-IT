---
title: Visualizzazione zoom
description: In modalità zoom continuo, la visualizzazione principale è costituita dall’immagine zoomabile quando la risorsa corrente è una singola immagine.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Visualizzazione zoom{#zoom-view}

In modalità zoom continuo, la visualizzazione principale è costituita dall’immagine zoomabile quando la risorsa corrente è una singola immagine.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato con il seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo nel formato esadecimale della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursore </span> </p> </td> 
   <td colname="col2"> <p>Cursore visualizzato sulla vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio : per rendere trasparente la visualizzazione dello zoom.

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

Nei sistemi desktop, il componente supporta `cursortype` selettore di attributi che può essere applicato al `.s7zoomview` classe. Controlla il tipo di cursore in base allo stato del componente e all&#39;azione dell&#39;utente. I seguenti `cursortype` sono supportati:

* `default`

   Visualizzato quando l&#39;immagine non è zoomabile a causa di una piccola risoluzione dell&#39;immagine, delle impostazioni dei componenti o di entrambe.

* `zoomin`

   Visualizzato quando l&#39;immagine può essere ingrandita.

* `reset`

   Visualizzata quando l&#39;immagine è al livello di zoom massimo e può essere ripristinata al suo stato iniziale.

* `drag`

   Visualizzato quando l&#39;utente fa un panning dell&#39;immagine con lo stato di zoom.

* `slide`

   Visualizzato quando l’utente esegue lo scambio di immagini facendo un tocco o uno sfarfallio orizzontale.
