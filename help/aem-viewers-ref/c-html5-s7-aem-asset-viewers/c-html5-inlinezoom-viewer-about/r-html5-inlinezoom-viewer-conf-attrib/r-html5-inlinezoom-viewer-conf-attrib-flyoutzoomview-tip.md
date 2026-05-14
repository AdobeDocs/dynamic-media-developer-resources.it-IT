---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
TQID: 'https://experienceleague.adobe.com/KJkYYAJzpCL1oSSZCOIDOQjzZ4igTS2ZBoruO-GM9mQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`durata`*[, *`conteggio`*][, *`dissolvenza`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durata</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica per quanti secondi viene visualizzato il testo della descrizione prima che venga nascosto. Se è impostato su <span class="codeph"> -1</span>, il messaggio viene sempre visualizzato, anche se l'utente attiva l'elemento a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> conteggio</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica quante volte viene visualizzato il testo quando si visualizzano nuove immagini nel set. Il valore <span class="codeph"> -1</span> indica che il testo viene sempre visualizzato quando si visualizzano immagini nel set. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dissolvenza <span class="codeph"> <span class="varname"></span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata di un'animazione di dissolvenza che si verifica quando il testo compare o scompare. Un valore di <span class="codeph"> 0</span> indica nessuna transizione di dissolvenza. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
