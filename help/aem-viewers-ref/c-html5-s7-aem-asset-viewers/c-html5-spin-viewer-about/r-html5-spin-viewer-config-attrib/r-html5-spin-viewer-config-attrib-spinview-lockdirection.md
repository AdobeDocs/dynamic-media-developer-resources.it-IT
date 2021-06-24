---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set 360 gradi
role: Developer,Business Practitioner
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '132'
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
