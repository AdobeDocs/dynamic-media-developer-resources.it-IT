---
title: FlyoutZoomView.frametransition
description: FlyoutZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 39cb629a-3940-4206-91cd-fe9a9f4d9f75
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 5%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`durata`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nessuno|dissolvenza</span> </p> </td> 
   <td colname="col2"> <p> </p> <p> Specifica il tipo di effetto applicato alla vista principale al cambiamento di risorsa. </p> <p><span class="codeph"> none</span> sta per nessuna transizione; la modifica della visualizzazione principale avviene immediatamente. </p> <p><span class="codeph"> dissolvenza</span> attiva la transizione di dissolvenza incrociata tra la scomparsa della prima immagine e la comparsa della nuova immagine </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Durata <span class="codeph"><span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> Numero di secondi richiesti per il completamento dell'animazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

Nessuno.

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`frametransition=fade,1`
