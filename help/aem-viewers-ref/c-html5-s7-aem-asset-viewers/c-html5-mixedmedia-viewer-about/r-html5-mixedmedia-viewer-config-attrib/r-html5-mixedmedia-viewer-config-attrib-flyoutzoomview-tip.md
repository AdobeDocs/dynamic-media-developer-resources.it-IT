---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`durata`*[, *`count`*][, *`dissolvenza`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> durata</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica per quanti secondi viene visualizzato il testo della descrizione prima che venga nascosto. Se impostato su <span class="codeph"> -1</span>, il messaggio viene sempre visualizzato, anche se l’utente attiva l’elemento a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica quante volte viene visualizzato il testo quando si visualizzano nuove immagini nel set. Un valore di <span class="codeph"> -1</span> significa che il testo viene sempre visualizzato quando si visualizzano le immagini del set. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dissolvenza</span></span> </p> </td> 
   <td colname="col2"> Specifica la durata di un'animazione di dissolvenza che si verifica quando il testo compare o scompare. Un valore di <span class="codeph"> 0</span> indica nessuna transizione di dissolvenza. </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
