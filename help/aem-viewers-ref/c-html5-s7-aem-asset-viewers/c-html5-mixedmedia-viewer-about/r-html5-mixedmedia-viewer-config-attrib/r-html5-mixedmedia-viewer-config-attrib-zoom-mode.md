---
title: zoomMode
description: Imposta il tipo di interazione di zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# zoomMode{#zoommode}

Imposta il tipo di interazione di zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuo|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuo </span> consente lo zoom classico in cui l’immagine viene gradualmente ingrandita quando si fa clic, si tocca o si spegne la visualizzazione principale. Per tornare alla visualizzazione iniziale, ridurre o ripristinare lo stato di zoom. Classe </p> <p> <span class="codeph"> inline </span> consente lo zoom istantaneo, in cui l'immagine ingrandita appare istantaneamente quando si passa il mouse sulla vista principale sul desktop o si tocca e si tiene premuto su un dispositivo touch. L'immagine ritorna automaticamente allo stato iniziale dopo aver spostato il mouse dalla visualizzazione o rilasciato il dito. In <span class="codeph"> inline </span> i set di immagini nidificati vengono appiattiti e visualizzati come miniature individuali. Classe <span class="codeph"> auto </span> attiva la modalità in linea sul desktop e la modalità continua sui dispositivi touch. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
