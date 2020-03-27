---
description: 'null'
seo-description: 'null'
seo-title: TableOfContents.cuscinetto
solution: Experience Manager
title: TableOfContents.cuscinetto
topic: Dynamic media
uuid: 832ebacf-d57f-4efa-ab1a-6a454f7c7a32
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# TableOfContents.cuscinetto{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> Controlla la direzione dell’aspetto del pannello a discesa. </p> <p>Quando è impostato per l’ <span class="codeph"> adattamento verticale</span>, il componente sposta prima la posizione del pannello di base nella parte inferiore del pulsante e tenta di eseguire il rollout del pannello a destra o a sinistra dalla posizione di base. Per ogni tentativo, il componente verifica se il pannello è ritagliato da un contenitore esterno. Se tutti i tentativi non vanno a buon fine, il componente tenta di spostare la posizione del pannello di base verso l’alto e di ripetere i tentativi di implementazione nella direzione destra e sinistra. </p> <p>Quando è impostato per l' <span class="codeph"> adattamento laterale</span>, il componente utilizza una logica simile, ma sposta prima la base verso destra, provando verso il basso e verso l'alto le direzioni. Poi sposta la base a sinistra, cercando di abbassare e di alzare le direzioni. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Imposta il ritardo in secondi per il timer di disattivazione automatica del menu a discesa che nasconde il pannello quando un utente è inattivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-55436ddd78b04f538dbb9a7a8463feae}

Facoltativo.

## Predefinito {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## Esempio {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
