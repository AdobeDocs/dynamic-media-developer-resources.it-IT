---
description: Imposta il tipo di interazione di zoom.
solution: Experience Manager
title: zoomMode
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '141'
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
