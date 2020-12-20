---
description: 'null'
seo-description: 'null'
seo-title: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
topic: Dynamic media
uuid: b46a3d78-e381-4351-a4f4-a228386df527
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Specifica se consentire una modifica nella direzione di rotazione in caso di set 360 gradi 2D. </p> <p>Se impostato su <span class="codeph"> 1 </span>, il componente identifica la direzione di trascinamento o di scorrimento principale (orizzontale o verticale) all'inizio del gesto. Dopo di che, mantiene quella direzione fino alla fine del gesto. Ad esempio, se l’utente avvia una rotazione orizzontale e successivamente decide di continuare il movimento di trascinamento in direzione verticale, il componente non esegue una rotazione verticale; considera invece solo lo spostamento orizzontale del mouse o del passaggio del dito. </p> <p>Un valore di <span class="codeph"> 0 </span> consente a un utente di cambiare la direzione di rotazione in qualsiasi momento durante il movimento. L’impostazione non ha alcun effetto se il set 360 gradi è 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
