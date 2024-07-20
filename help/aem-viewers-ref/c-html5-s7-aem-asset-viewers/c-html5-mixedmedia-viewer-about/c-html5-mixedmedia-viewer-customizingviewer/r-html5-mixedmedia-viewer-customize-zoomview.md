---
title: Visualizzazione zoom
description: In modalità di zoom continuo, la vista principale è costituita dall’immagine zoomabile quando la risorsa corrente è una singola immagine.
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

In modalità di zoom continuo, la vista principale è costituita dall’immagine zoomabile quando la risorsa corrente è una singola immagine.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato dal seguente selettore di classi CSS:

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
   <td colname="col2"> <p> Colore di sfondo in formato esadecimale della visualizzazione principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursore </span> </p> </td> 
   <td colname="col2"> <p>Cursore visualizzato sopra la vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la visualizzazione zoom.

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

Nei sistemi desktop il componente supporta il selettore di attributi `cursortype` che può essere applicato alla classe `.s7zoomview`. Controlla il tipo di cursore in base allo stato del componente e all’azione dell’utente. Sono supportati i seguenti valori `cursortype`:

* `default`

  Visualizzato quando l&#39;immagine non è ingrandita a causa di una risoluzione ridotta dell&#39;immagine, di impostazioni dei componenti o di entrambi.

* `zoomin`

  Viene visualizzato quando è possibile ingrandire l&#39;immagine.

* `reset`

  Viene visualizzata quando l&#39;immagine è al massimo livello di zoom e può essere ripristinata allo stato iniziale.

* `drag`

  Viene visualizzato quando l’utente effettua una panoramica dell’immagine ingrandita.

* `slide`

  Viene visualizzato quando l&#39;utente esegue lo scambio di immagini eseguendo uno scorrimento orizzontale.
