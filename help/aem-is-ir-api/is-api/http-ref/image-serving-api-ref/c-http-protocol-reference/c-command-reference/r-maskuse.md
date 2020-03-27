---
description: Utilizzo della maschera immagine. Specifica in che modo la maschera o il canale alfa dell’immagine viene utilizzato per le operazioni sull’immagine (ad esempio, colorize=). Se specificato in un livello di effetto, consente di applicare l’effetto all’area di sfondo del livello principale o all’intero rettangolo del livello principale.
seo-description: Utilizzo della maschera immagine. Specifica in che modo la maschera o il canale alfa dell’immagine viene utilizzato per le operazioni sull’immagine (ad esempio, colorize=). Se specificato in un livello di effetto, consente di applicare l’effetto all’area di sfondo del livello principale o all’intero rettangolo del livello principale.
seo-title: maskUse
solution: Experience Manager
title: maskUse
topic: Scene7 Image Serving - Image Rendering API
uuid: 2c70da87-f869-495a-be50-226a4516e002
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# maskUse{#maskuse}

Utilizzo della maschera immagine. Specifica in che modo la maschera o il canale alfa dell’immagine viene utilizzato per le operazioni sull’immagine (ad esempio, colorize=). Se specificato in un livello di effetto, consente di applicare l’effetto all’area di sfondo del livello principale o all’intero rettangolo del livello principale.

`maskUse=norm|invert|off`

Nella tabella seguente è illustrato l’effetto di `maskUse=` varia a seconda della disponibilità e del tipo di maschera (canale alfa) associata all’immagine del livello.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Valore</b> </th> 
   <th class="entry"> <b> Nessuna maschera</b> </th> 
   <th class="entry"> <b> Alfa non associato (o immagine maschera separata)</b> </th> 
   <th class="entry"> <b> Alfa associata (premoltiplicata)</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> off </span> </p> </td> 
   <td> <p> Rettangolo immagine opaco </p> </td> 
   <td> <p> Rettangolo immagine opaco </p> </td> 
   <td> <p> Area di primo piano dell’immagine su un rettangolo riempito di nero pieno </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> norma </span> </p> </td> 
   <td> <p> Rettangolo immagine opaco </p> </td> 
   <td> <p> Area di primo piano dell’immagine </p> </td> 
   <td> <p> Area di primo piano dell’immagine o del livello </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> invertito </span> </p> </td> 
   <td> <p> Livello nascosto </p> </td> 
   <td> <p> Area di sfondo dell’immagine </p> </td> 
   <td> <p> Area di sfondo dell’immagine o livello riempita con nero in tinta unita </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f36ad1af348e45aeb3eb336544df30b0}

Attributo immagine o livello. Si applica al livello 0 se `layer=comp`. Se specificato in un livello di effetto, il comando modifica la maschera ereditata dal livello principale.

Il comportamento di non `maskUse=` è definito e non è supportato se specificato con livelli di testo o di colore in tinta unita quando non è applicabile alcuna maschera immagine (specificata con `mask=` o `catalog::Mask`).

## Predefinito {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Esempio {#section-daa371e9be5547368ff6772342acba0a}

Colorare l’area di sfondo di un’immagine; il primo piano dell’immagine è definito da un’immagine maschera separata. A questo scopo, sovrapponete lo sfondo colorato dell’immagine se l’immagine non è stata modificata:

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## Consultate anche {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
