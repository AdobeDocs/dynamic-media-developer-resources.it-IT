---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---


# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Specifica se consentire una modifica nella direzione di rotazione in caso di set di rotazione 2D. </p> <p>Quando è impostato su <span class="codeph"> 1 </span>, il componente identifica la direzione di trascinamento o scorrimento principale (orizzontale o verticale) all'inizio del gesto. Dopodiché, mantiene quella direzione fino alla fine del gesto. Ad esempio, se l’utente avvia una rotazione orizzontale e decide di continuare il movimento di trascinamento in direzione verticale, il componente non esegue una rotazione verticale; invece, considera solo il movimento orizzontale del mouse o del ronzio. </p> <p>Un valore di <span class="codeph"> 0 </span> consente a un utente di cambiare la direzione di centrifuga in qualsiasi momento durante l'avanzamento del gesto. L'impostazione non ha alcun effetto se il set 360 gradi è 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
