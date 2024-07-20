---
title: Visualizzazione zoom
description: La vista principale è costituita dall'immagine ingrandita.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Visualizzazione zoom{#zoom-view}

La vista principale è costituita dall&#39;immagine ingrandita.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato dal seguente selettore di classi CSS:

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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo in formato esadecimale della visualizzazione principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursore </span> </p> </td> 
   <td colname="col2"> <p>Cursore visualizzato sopra la vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la visualizzazione principale.

```
.s7zoomviewer .s7zoomview { 
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
