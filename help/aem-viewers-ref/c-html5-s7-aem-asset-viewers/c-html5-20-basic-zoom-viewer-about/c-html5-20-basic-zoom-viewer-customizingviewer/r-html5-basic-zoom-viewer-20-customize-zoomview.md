---
title: Visualizzazione zoom
description: La vista principale è costituita dall'immagine ingrandita.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 286b9df4-88db-4e5d-aab4-9cbe01195e57
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---

# Visualizzazione zoom{#zoom-view}

La vista principale è costituita dall&#39;immagine ingrandita.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato dal seguente selettore di classi CSS:

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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo in formato esadecimale della visualizzazione principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursore </span> </p> </td> 
   <td colname="col2"> <p>Il cursore viene visualizzato sopra la vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la visualizzazione principale.

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Nei sistemi desktop il componente supporta il selettore di attributi `cursortype` che può essere applicato alla classe `.s7zoomview` e controlla il tipo di cursore in base allo stato del componente e all&#39;azione dell&#39;utente. Sono supportati i seguenti valori `cursortype`:

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valore </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> predefinito </span> </p> </td> 
   <td colname="col2"> <p>Visualizzato quando l'immagine non è ingrandita a causa di una risoluzione ridotta dell'immagine, di impostazioni dei componenti o di entrambi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Zoom <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Viene visualizzato quando è possibile ingrandire l'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ha reimpostato </span> </p> </td> 
   <td colname="col2"> <p>Viene visualizzata quando l'immagine è al massimo livello di zoom e può essere ripristinata allo stato iniziale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trascinare </span> </p> </td> 
   <td colname="col2"> <p>Viene visualizzato quando un utente effettua una panoramica dell’immagine ingrandita. </p> </td> 
  </tr> 
 </tbody> 
</table>
