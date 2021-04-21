---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---


# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`dividerWidthdividerColordividerOpacityborderOnOffborderColorfillColor`*`

Controlla l’aspetto del componente quando un `PageView.frametransition` è impostato su `turn` o su `auto` sui sistemi desktop.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> Larghezza in pixel dell’ombreggiatura del divisore di pagina che separa le pagine sinistra e destra nel set di pagine affiancate. Controlla anche la larghezza dell'ombreggiatura in esecuzione visualizzata accanto alla pagina di tornitura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> Colore dell'ombra in formato RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>L'opacità dell'ombreggiatura nell'intervallo compreso tra <span class="codeph"> 0</span> e <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> Flag (<span class="codeph"> 0</span> o <span class="codeph"> 1</span>) che attiva e disattiva il bordo intorno alla pagina di accensione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> Colore del bordo in formato RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> Colore del riempimento a tinta unita dell’area del componente utilizzata durante l’animazione del giro della pagina, in formato RRGGBB. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-54c634116cfe4f17813318e07539264c}

Facoltativo.

## Predefinito {#section-43fd13f639c2480c82658fafeeaf0846}

`40,909090,1,1,909090,FFFFFF`

## Esempi {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
