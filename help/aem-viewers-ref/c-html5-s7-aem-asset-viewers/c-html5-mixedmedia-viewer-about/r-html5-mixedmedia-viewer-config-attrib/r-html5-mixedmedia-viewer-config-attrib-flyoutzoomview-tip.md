---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
TQID: 'https://experienceleague.adobe.com/Pnrb2IBaQgvQL2acyGn7eJuCy1ko0ok42azq9b2y50w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`durata`*[, *`conteggio`*][, *`dissolvenza`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Durata <span class="codeph"><span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> Specifica per quanti secondi viene visualizzato il testo della descrizione prima che venga nascosto. Se è impostato su <span class="codeph"> -1</span>, il messaggio viene sempre visualizzato, anche se l'utente attiva l'elemento a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> conteggio</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica quante volte viene visualizzato il testo quando si visualizzano nuove immagini nel set. Il valore <span class="codeph"> -1</span> indica che il testo viene sempre visualizzato quando si visualizzano immagini nel set. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dissolvenza <span class="codeph"><span class="varname"></span></span> </p> </td> 
   <td colname="col2"> Specifica la durata di un'animazione di dissolvenza che si verifica quando il testo compare o scompare. Il valore <span class="codeph"> 0</span> indica nessuna transizione di dissolvenza. </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
