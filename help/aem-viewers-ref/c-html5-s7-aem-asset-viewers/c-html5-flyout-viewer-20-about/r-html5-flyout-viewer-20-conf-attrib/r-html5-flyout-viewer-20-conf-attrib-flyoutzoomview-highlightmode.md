---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> evidenziazione|cursore </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di frame di navigazione da utilizzare. Se è impostato su <span class="codeph"> cursore </span>, il componente utilizza un cursore di riferimento di dimensione fissa. È possibile utilizzare un cursore art diverso per i sistemi desktop e i dispositivi touch. Questa funzionalità è controllata con la classe CSS <span class="codeph"> .s7cursor </span> e il selettore di attributi <span class="codeph"> input=mouse|touch </span>. Nei sistemi desktop, viene impostato un punto di ancoraggio al centro dell'area del cursore, mentre nei dispositivi touch l'ancoraggio si trova al centro inferiore del cursore. Se è impostato su <span class="codeph">, evidenzia </span>, il componente utilizza un frame di navigazione di dimensioni variabili; le dimensioni e la forma del frame dipendono dal fattore di zoom e dalle dimensioni della visualizzazione a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> Imposta il tempo (in secondi) di dissolvenza in entrata dell'evidenziazione o del cursore dopo l'attivazione da parte dell'utente. La dissolvenza in entrata viene applicata solo ai dispositivi touch; sui sistemi desktop viene ignorata dal componente. </p> <p>La dissolvenza in entrata si applica ai seguenti elementi dell'interfaccia utente: frame di evidenziazione, cursore fisso, sovrapposizione (se il parametro <span class="codeph"> della sovrapposizione </span> è impostato su <span class="codeph"> 1 </span>). L'animazione della vista a comparsa inizia solo dopo la dissolvenza di evidenziazione/cursore al termine dell'animazione. Non è presente alcuna animazione di dissolvenza in uscita. Quando l’utente disattiva il riquadro a comparsa, gli elementi corrispondenti dell’interfaccia utente (cursore, evidenziazione e sovrapposizione) si nascondono immediatamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|libero </span> </p> </td> 
   <td colname="col2"> <p> Controlla il posizionamento del frame di navigazione. </p> <p>Se è impostato su <span class="codeph"> per l'immagine </span>, il frame di navigazione può essere posizionato solo all'interno dell'area immagine effettiva all'interno della visualizzazione principale. </p> <p>Se è impostato su <span class="codeph"> liberi </span>, un utente può spostare il frame di navigazione in qualsiasi punto dell'area di visualizzazione principale logica, anche al di fuori del contenuto dell'immagine. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
