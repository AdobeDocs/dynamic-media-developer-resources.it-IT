---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
topic: Dynamic media
uuid: 397c1af0-f806-4555-83fa-ec7548b59a60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 1%

---


# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> highlight|cursor  </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di cornice di navigazione da utilizzare. Se impostato su <span class="codeph"> cursore </span>, il componente utilizza un cursore di riferimento a dimensione fissa. È possibile che la grafica del cursore sia diversa per i sistemi desktop e i dispositivi touch, questo è controllato con la classe CSS <span class="codeph"> .s7cursor </span> e <span class="codeph"> input=mouse|touch </span> selettore di attributi. Sui sistemi desktop, un punto di ancoraggio è impostato al centro dell'area del cursore, mentre sui dispositivi touch l'ancoraggio si trova al centro inferiore del cursore. Se impostato su <span class="codeph"> evidenzia </span>, il componente utilizza un frame di navigazione a dimensione variabile; le dimensioni e la forma del fotogramma dipendono dal fattore di zoom e dalle dimensioni della visualizzazione a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> Imposta il tempo (in secondi) per cui l’evidenziazione o il cursore vengono dissolti dopo che l’utente l’ha attivata. La dissolvenza in entrata è applicata solo sui dispositivi touch; nei sistemi desktop viene ignorato dal componente. </p> <p>La dissolvenza in entrata si applica ai seguenti elementi dell’interfaccia: fotogramma di evidenziazione, cursore fisso, sovrapposizione (nel caso in cui il parametro <span class="codeph"> della sovrapposizione </span> sia impostato su <span class="codeph"> 1 </span>). L'animazione della visualizzazione a comparsa inizia solo dopo il completamento dell'evidenziazione o della dissolvenza del cursore nell'animazione. Non esiste animazione con dissolvenza in uscita. Quando l’utente disattiva il menu a comparsa, gli elementi dell’interfaccia utente corrispondenti (cursore, evidenziazione e sovrapposizione) si nascondono all’istante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free  </span> </p> </td> 
   <td colname="col2"> <p> Controlla il posizionamento del frame di navigazione. </p> <p>Se impostato su <span class="codeph"> onimage </span>, la cornice di navigazione può essere posizionata solo all'interno dell'area dell'immagine effettiva all'interno della vista principale. </p> <p>Se impostato su <span class="codeph"> gratuito </span>, un utente può spostare il frame di navigazione ovunque nell'area di visualizzazione principale logica, anche all'esterno del contenuto dell'immagine. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
