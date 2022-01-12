---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`spettacolo`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> evidenziatore|cursore </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di frame di navigazione da utilizzare. Quando è impostato su <span class="codeph"> cursore </span>, il componente utilizza un cursore di riferimento a dimensione fissa. È possibile avere diverse immagini del cursore per i sistemi desktop e i dispositivi touch. Questa capacità è controllata con <span class="codeph"> .s7cursor </span> Classe CSS e <span class="codeph"> input=mouse|touch </span> selettore di attributi. Nei sistemi desktop, un punto di ancoraggio è impostato al centro dell'area del cursore, mentre sui dispositivi touch l'ancoraggio è al centro inferiore del cursore. Quando è impostato su <span class="codeph"> highlight </span>, il componente utilizza un riquadro di navigazione a dimensione variabile; le dimensioni e la forma del fotogramma dipendono dal fattore di zoom e dalle dimensioni della visualizzazione a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spettacolo </span> </span> </p> </td> 
   <td colname="col2"> <p> Imposta il tempo (in secondi) in cui l’evidenziazione o il cursore vengono sfumati dopo l’attivazione da parte dell’utente. La dissolvenza in entrata viene applicata solo sui dispositivi touch; sui sistemi desktop viene ignorato dal componente. </p> <p>La dissolvenza in si applica ai seguenti elementi dell’interfaccia utente: evidenziatore, cursore fisso, sovrapposizione (nel caso <span class="codeph"> sovrapposizione </span> è impostato su <span class="codeph"> 1 </span>). L’animazione della visualizzazione a comparsa inizia solo al termine della dissolvenza dell’evidenziazione/cursore nell’animazione. Non c'è animazione dissolvenza in uscita. Quando l’utente disattiva il riquadro a comparsa, gli elementi corrispondenti dell’interfaccia (cursore, evidenziazione e sovrapposizione) vengono nascosti istantaneamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> Controlla il posizionamento del frame di navigazione. </p> <p>Se impostato su <span class="codeph"> onimage </span>, il riquadro di navigazione può essere posizionato solo all'interno dell'area dell'immagine effettiva all'interno della vista principale. </p> <p>Se impostato su <span class="codeph"> gratuito </span> un utente può spostare il frame di navigazione in qualsiasi punto dell'area di visualizzazione principale logica, anche all'esterno del contenuto dell'immagine. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
