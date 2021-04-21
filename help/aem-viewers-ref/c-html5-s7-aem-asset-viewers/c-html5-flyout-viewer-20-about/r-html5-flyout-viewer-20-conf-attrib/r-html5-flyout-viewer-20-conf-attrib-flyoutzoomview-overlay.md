---
description: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 4%

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Controlla l'aspetto dell'evidenziazione della vista principale quando il riquadro a comparsa è attivo. Quando è impostata su <span class="codeph"> 0</span>, l'area attualmente visibile nella finestra a comparsa viene evidenziata utilizzando gli stili forniti dal modificatore <span class="codeph"> .s7highlight</span> o <span class="codeph"> .s7cursor</span> CSS (a seconda del valore del modificatore <span class="codeph"> highlightMode</span>). Quando è impostato su <span class="codeph"> 1</span> il componente entra in modalità "inverse" dove l'area correntemente visualizzata è completamente trasparente (nel caso in cui <span class="codeph"> highlightMode</span> sia impostato su <span class="codeph"> highlight</span>) o formattata con <span class="codeph"> .s7cursor</span> il nome della classe CSS (nel caso in cui sia impostato <span class="codeph"> highlight mode</span>) a <span class="codeph"> cursore</span>), ma l'area circostante viene riempita utilizzando gli stili forniti da <span class="codeph"> .s7overlay</span> nome della classe CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
