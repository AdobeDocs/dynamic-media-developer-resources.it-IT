---
title: wid
description: Larghezza visualizzazione. Specifica la larghezza dell'immagine di risposta (immagine di visualizzazione).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# wid{#wid}

Larghezza visualizzazione. Specifica la larghezza dell&#39;immagine di risposta (immagine di visualizzazione).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Larghezza dell’immagine in pixel (int maggiore di 0) </p></td> 
 </tr> 
</table>

## Predefinito {#section-830bae0b6bac440098444d7cdcb23e2e}

Se nessuno dei due `wid=`, `hei=`, né `scale=` , l&#39;immagine di risposta corrisponde alle dimensioni di visualizzazione predefinite specificate nel file FXG.

Il rendering dei formati raster viene eseguito utilizzando l&#39;impostazione Default View Size (o DefaultPix). Clic **[!UICONTROL Impostazione applicazione]** > **[!UICONTROL Impostazione pubblicazione]** > **[!UICONTROL Server immagini]**, quindi immettere i valori di larghezza e altezza. Le dimensioni più piccole offrono prestazioni migliori. Salva le impostazioni ed esegui una pubblicazione Image Server per applicare una modifica.

Se si applica una `scale=1` viene eseguito il rendering di una richiesta di formato raster alle dimensioni specificate in FXG.

## Esempio {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

A meno che non sia specificato un formato, l&#39;immagine viene riprodotta come file SWF. In questo caso, l’altezza e la larghezza non hanno alcun significato, perché il SWF di solito si espande fino alle dimensioni della finestra del browser. Di conseguenza, `hei` e `wid` si applica solo ai formati raster o PDF. I formati raster includono:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa
