---
title: PageView.pageturnstyle
description: PageView.pageturnstyle
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 00706c64-c051-4b62-8194-61d0a1c565e9
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *`dividerWidth`*, *`dividerColor`*, *`dividerOpacity`*, *`borderOnOff`*, *`borderColor`*, *`fillColor`*`

Controlla l&#39;aspetto del componente quando `PageView.frametransition` è impostato su `turn` o su `auto` nei sistemi desktop.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> Larghezza in pixel dell'ombreggiatura del divisore di pagina che separa le pagine sinistra e destra nella distribuzione. Controlla inoltre la larghezza dell'ombreggiatura in esecuzione visualizzata accanto alla pagina di tornitura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>DivderOpacity <span class="codeph"><span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> Colore dell'ombreggiatura in formato RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>DivderOpacity <span class="codeph"><span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p>Opacità dell'ombreggiatura compresa tra <span class="codeph"> 0</span> e <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> Flag (<span class="codeph"> 0</span> o <span class="codeph"> 1</span>) che attiva e disattiva il bordo attorno alla pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> Colore del bordo in formato RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> Colore del riempimento a tinta unita dell'area dei componenti utilizzata durante l'animazione di volta pagina, in formato RGGBB. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-54c634116cfe4f17813318e07539264c}

Facoltativo.

## Predefinito {#section-43fd13f639c2480c82658fafeeaf0846}

`40,909090,1,1,909090,FFFFFF`

## Esempi {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
