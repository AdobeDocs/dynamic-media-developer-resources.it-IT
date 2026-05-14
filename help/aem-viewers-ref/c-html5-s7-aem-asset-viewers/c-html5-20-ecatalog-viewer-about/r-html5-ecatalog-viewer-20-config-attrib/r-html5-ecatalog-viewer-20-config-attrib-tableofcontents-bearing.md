---
title: Sommario.cuscinetto
description: Sommario.cuscinetto
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
TQID: 'https://experienceleague.adobe.com/i8oPW8fpqvU8JaUaJ-95swaFjD6YTHcqv21s3i7-L2g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 1%

---

# Sommario.cuscinetto{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> Controlla la direzione dell'aspetto del pannello a discesa. </p> <p>Se è impostato su <span class="codeph"> adatta a verticale</span>, il componente sposta prima la posizione del pannello di base nella parte inferiore del pulsante e tenta di stendere il pannello a destra o a sinistra dalla posizione di base. A ogni tentativo, il componente controlla se il pannello è ritagliato da un contenitore esterno. Se tutti i tentativi hanno esito negativo, il componente tenta di spostare la posizione del pannello di base verso l’alto e ripetere i tentativi di rollout nelle direzioni destra e sinistra. </p> <p>Se è impostato su <span class="codeph"> fit-lateral</span>, il componente utilizza una logica simile, ma sposta la base a destra per prima, provando le direzioni di rollout verso il basso e verso l'alto. Quindi, sposta la base a sinistra, provando le direzioni di rollout verso il basso e verso l'alto. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Imposta il ritardo in secondi per il timer di Nascondi automatico a discesa che nasconde il pannello quando un utente è inattivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-55436ddd78b04f538dbb9a7a8463feae}

Facoltativo.

## Predefinito {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## Esempio {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
