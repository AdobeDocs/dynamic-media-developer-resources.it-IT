---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.highlightMode
solution: Experience Manager
title: FlyoutZoomView.highlightMode
topic: Dynamic media
uuid: 397c1af0-f806-4555-83fa-ec7548b59a60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.highlightMode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> highlight|cursor </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di cornice di navigazione da utilizzare. Quando è impostato su <span class="codeph"> cursore, </span>il componente utilizza un cursore di riferimento a dimensione fissa. È possibile avere grafica del cursore diversa per i sistemi desktop e i dispositivi touch, questo è controllato con classe <span class="codeph"> .s7cursor </span> CSS e <span class="codeph"> input=mouse|touch </span> attributo selettore. Sui sistemi desktop, un punto di ancoraggio è impostato al centro dell'area del cursore, mentre sui dispositivi touch l'ancoraggio si trova al centro inferiore del cursore. Quando è impostato per l’ <span class="codeph"> evidenziazione, </span>il componente utilizza un frame di navigazione a dimensione variabile; le dimensioni e la forma del fotogramma dipendono dal fattore di zoom e dalle dimensioni della visualizzazione a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span></span> </p> </td> 
   <td colname="col2"> <p> Imposta il tempo (in secondi) per cui l’evidenziazione o il cursore vengono dissolti dopo che l’utente l’ha attivata. La dissolvenza in entrata è applicata solo sui dispositivi touch; nei sistemi desktop viene ignorato dal componente. </p> <p>La dissolvenza in entrata si applica ai seguenti elementi dell’interfaccia: fotogramma di evidenziazione, cursore fisso, sovrapposizione (nel caso <span class="codeph"> in cui il </span> parametro di sovrapposizione sia impostato su <span class="codeph"> 1 </span>). L'animazione della visualizzazione a comparsa inizia solo dopo il completamento dell'evidenziazione o della dissolvenza del cursore nell'animazione. Non esiste animazione con dissolvenza in uscita. Quando l’utente disattiva il menu a comparsa, gli elementi dell’interfaccia utente corrispondenti (cursore, evidenziazione e sovrapposizione) si nascondono all’istante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> Controlla il posizionamento del frame di navigazione. </p> <p>Se impostato su <span class="codeph"> un'immagine, </span> la cornice di navigazione può essere posizionata solo all'interno dell'area dell'immagine effettiva all'interno della vista principale. </p> <p>Se impostato su <span class="codeph"> gratuito, </span> l'utente può spostare la cornice di navigazione ovunque nell'area di visualizzazione principale logica, anche all'esterno del contenuto dell'immagine. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
