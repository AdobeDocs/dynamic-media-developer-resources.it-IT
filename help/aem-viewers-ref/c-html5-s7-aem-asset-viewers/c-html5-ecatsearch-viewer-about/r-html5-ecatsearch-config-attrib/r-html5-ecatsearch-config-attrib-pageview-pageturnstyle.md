---
description: 'null'
seo-description: 'null'
seo-title: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
topic: Dynamic media
uuid: 748adb73-bfb6-4fce-aa6a-4216184edabb
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`dividerWidthdividerColordividerOpacityborderOnOffborderColorfillColor`*`]

Controlla l’aspetto del componente quando [!DNL `PageView.frametransition`] è impostato su [!DNL `turn`] o su [!DNL `auto`] sui sistemi desktop.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> Larghezza in pixel dell’ombra del separatore di pagina che separa le pagine sinistra e destra del set di pagine affiancate. Controlla anche la larghezza dell’ombra esterna visualizzata accanto alla pagina di tornitura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> Colore ombra in formato RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>L’opacità dell’ombra nell’intervallo da <span class="codeph"> 0</span> a <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> Flag ( <span class="codeph"> 0</span> o <span class="codeph"> 1</span>) che attiva e disattiva il bordo intorno alla pagina di attivazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> Colore del bordo in formato RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> Colore del riempimento in tinta unita dell’area del componente utilizzata durante l’animazione del giro di pagina, in formato RRGGBB. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-54c634116cfe4f17813318e07539264c}

Facoltativo.

## Predefinito {#section-43fd13f639c2480c82658fafeeaf0846}

[!DNL `40,909090,1,1,909090,FFFFFF`]

## Esempi {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
