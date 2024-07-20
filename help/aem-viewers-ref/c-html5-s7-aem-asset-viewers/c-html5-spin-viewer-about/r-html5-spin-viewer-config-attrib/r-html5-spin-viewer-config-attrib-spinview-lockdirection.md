---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Specifica se consentire una modifica della direzione di rotazione in presenza di un set di rotazione 2D. </p> <p>Se è impostato su <span class="codeph"> 1 </span>, il componente identifica la direzione di trascinamento o scorrimento principale (orizzontale rispetto a verticale) all'inizio del movimento. Dopo di che, essa mantiene tale direzione fino alla fine del gesto. Ad esempio, se l’utente avvia una rotazione orizzontale e poi decide di continuare il movimento di trascinamento in direzione verticale, il componente non esegue una rotazione verticale. Considera invece solo il movimento orizzontale del mouse o del passaggio. </p> <p>Un valore di <span class="codeph"> 0 </span> consente a un utente di cambiare la direzione di rotazione in qualsiasi momento durante l'avanzamento del movimento. L'impostazione non ha effetto se il set 360 gradi è 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
