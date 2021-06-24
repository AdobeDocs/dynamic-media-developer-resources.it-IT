---
description: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
feature: Dynamic Media Classic,Visualizzatori,SDK/API,A comparsa
role: Developer,Business Practitioner
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`spettacolo`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> evidenziatore|cursore  </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di frame di navigazione da utilizzare. Quando è impostato su <span class="codeph"> cursore </span>, il componente utilizza un cursore di riferimento a dimensione fissa. È possibile avere una grafica del cursore diversa per i sistemi desktop e i dispositivi touch, è controllato con <span class="codeph"> .s7cursor </span> classe CSS e <span class="codeph"> input=mouse|touch </span> selettore di attributi. Nei sistemi desktop, un punto di ancoraggio viene impostato al centro dell'area del cursore, mentre sui dispositivi touch l'ancoraggio si trova al centro inferiore del cursore. Se impostato su <span class="codeph"> evidenzia </span>, il componente utilizza un frame di navigazione a dimensione variabile; le dimensioni e la forma del fotogramma dipendono dal fattore di zoom e dalle dimensioni della visualizzazione a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spettacolo  </span> </span> </p> </td> 
   <td colname="col2"> <p> Imposta il tempo (in secondi) in cui l’evidenziazione o il cursore vengono sfumati dopo l’attivazione da parte dell’utente. La dissolvenza in entrata viene applicata solo sui dispositivi touch; sui sistemi desktop viene ignorato dal componente. </p> <p>La dissolvenza in si applica ai seguenti elementi dell’interfaccia utente: evidenziatore frame, cursore fisso, sovrapposizione (nel caso in cui il parametro <span class="codeph"> sovrapposizione </span> sia impostato su <span class="codeph"> 1 </span>). L’animazione della visualizzazione a comparsa inizia solo al termine della dissolvenza dell’evidenziazione/cursore nell’animazione. Non c'è animazione dissolvenza in uscita. Quando l’utente disattiva il riquadro a comparsa, gli elementi corrispondenti dell’interfaccia (cursore, evidenziazione e sovrapposizione) vengono nascosti istantaneamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free  </span> </p> </td> 
   <td colname="col2"> <p> Controlla il posizionamento del frame di navigazione. </p> <p>Se impostato su <span class="codeph"> onimage </span>, il frame di navigazione può essere posizionato solo all'interno dell'area immagine effettiva all'interno della vista principale. </p> <p>Se impostato su <span class="codeph"> gratuito </span>, un utente può spostare il frame di navigazione in qualsiasi punto dell'area di visualizzazione principale logica, anche all'esterno del contenuto dell'immagine. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
