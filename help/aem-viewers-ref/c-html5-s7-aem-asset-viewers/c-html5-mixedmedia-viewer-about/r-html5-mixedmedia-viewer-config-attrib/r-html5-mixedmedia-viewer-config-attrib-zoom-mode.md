---
title: zoomMode
description: Imposta il tipo di interazione di zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
TQID: 'https://experienceleague.adobe.com/Joa1KBx6spGvXsMkjxSCPn-23cICUffLJ9CWOQ-BRwo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 2%

---

# zoomMode{#zoommode}

Imposta il tipo di interazione di zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuo </span> abilita lo zoom classico in cui l'immagine si ingrandisce gradualmente quando si fa clic, si tocca due volte o si pizzica l'immagine nella visualizzazione principale. Per tornare alla visualizzazione iniziale, ridurre o ripristinare lo stato di zoom. La classe </p> <p> <span class="codeph"> inline </span> abilita lo zoom istantaneo, in cui l'immagine ingrandita viene visualizzata immediatamente quando si passa il puntatore del mouse sulla visualizzazione principale sul desktop o quando si tocca e si tiene premuto un dispositivo touch. L'immagine torna automaticamente allo stato iniziale dopo aver spostato il mouse dalla vista o aver rilasciato il dito. In modalità </span> in linea <span class="codeph">, i set di immagini nidificati vengono appiattiti e visualizzati come singole miniature. La classe <span class="codeph"> auto </span> attiva la modalità in linea sul desktop e la modalità continua sui dispositivi touch. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
