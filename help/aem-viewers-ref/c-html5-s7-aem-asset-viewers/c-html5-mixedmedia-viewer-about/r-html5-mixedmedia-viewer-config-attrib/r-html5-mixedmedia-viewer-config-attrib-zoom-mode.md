---
description: Imposta il tipo di interazione di zoom.
solution: Experience Manager
title: zoomMode
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---


# zoomMode{#zoommode}

Imposta il tipo di interazione di zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuo|inline|auto  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continua  </span> consente lo zoom classico in cui l’immagine viene gradualmente ingrandita quando si fa clic, si tocca o si spegne la visualizzazione principale. Per tornare alla visualizzazione iniziale, è necessario ridurre esplicitamente lo stato di zoom o ripristinarlo. </p> <p> <span class="codeph"> lo zoom in linea  </span> consente di visualizzare istantaneamente l'immagine ingrandita quando si passa il mouse sulla vista principale sul desktop o si tocca e si tiene premuto su un dispositivo touch; l'immagine ritorna automaticamente allo stato iniziale quando si sposta il mouse dalla visualizzazione o si rilascia il dito. In modalità <span class="codeph"> in linea </span> i set di immagini nidificati vengono appiattiti e visualizzati come miniature individuali. <span class="codeph"> attiva automaticamente  </span> la modalità in linea sul desktop e la modalità continua sui dispositivi touch. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
