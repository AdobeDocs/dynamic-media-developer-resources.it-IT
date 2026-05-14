---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
TQID: 'https://experienceleague.adobe.com/eTB-wD8G7HGSDgohQn-FsCeFL1GHMBiqzNUtT3nw5n4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 127
ht-degree: 3%

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
