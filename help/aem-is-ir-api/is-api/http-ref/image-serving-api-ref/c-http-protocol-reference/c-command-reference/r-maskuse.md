---
description: Utilizzo della maschera immagine. Specifica come la maschera o il canale alfa dell'immagine viene utilizzato per le operazioni sull'immagine (ad esempio, colorize=). Se specificato in un livello di effetto, consente di applicare l'effetto all'area di sfondo del livello padre o all'intero rettangolo del livello padre.
solution: Experience Manager
title: maskUse
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---


# maskUse{#maskuse}

Utilizzo della maschera immagine. Specifica come la maschera o il canale alfa dell&#39;immagine viene utilizzato per le operazioni sull&#39;immagine (ad esempio, colorize=). Se specificato in un livello di effetto, consente di applicare l&#39;effetto all&#39;area di sfondo del livello padre o all&#39;intero rettangolo del livello padre.

`maskUse=norm|invert|off`

La tabella seguente illustra l’effetto di `maskUse=` a seconda della disponibilità e del tipo di maschera (canale alfa) associata all’immagine del livello.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Valore</b> </th> 
   <th class="entry"> <b> Nessuna maschera</b> </th> 
   <th class="entry"> <b> Alfa non associata (o immagine maschera separata)</b> </th> 
   <th class="entry"> <b> Alfa associata (pre-moltiplicata)</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> off  </span> </p> </td> 
   <td> <p> Rettangolo immagine opaco </p> </td> 
   <td> <p> Rettangolo immagine opaco </p> </td> 
   <td> <p> Area in primo piano dell'immagine su rettangolo piena di nero solido </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> norma  </span> </p> </td> 
   <td> <p> Rettangolo immagine opaco </p> </td> 
   <td> <p> Area in primo piano dell'immagine </p> </td> 
   <td> <p> Area in primo piano dell'immagine o del livello </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> invertire  </span> </p> </td> 
   <td> <p> Livello nascosto </p> </td> 
   <td> <p> Area di sfondo dell'immagine </p> </td> 
   <td> <p> Area di sfondo dell'immagine o del livello riempito con nero solido </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f36ad1af348e45aeb3eb336544df30b0}

Attributo immagine o livello. Si applica al livello 0 se `layer=comp`. Se specificato in un livello di effetto, il comando modifica la maschera ereditata dal livello principale.

Il comportamento di `maskUse=` non è definito e non è supportato se specificato con livelli di testo o di colore solido quando non è applicabile alcuna maschera immagine (specificato con `mask=` o `catalog::Mask`).

## Predefinito {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Esempio {#section-daa371e9be5547368ff6772342acba0a}

Colorare l&#39;area di sfondo di un&#39;immagine; il primo piano dell&#39;immagine è definito da un&#39;immagine maschera separata. Questo si ottiene sovrapponendo lo sfondo colorato dell&#39;immagine se l&#39;immagine non modificata:

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## Consultate anche {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
