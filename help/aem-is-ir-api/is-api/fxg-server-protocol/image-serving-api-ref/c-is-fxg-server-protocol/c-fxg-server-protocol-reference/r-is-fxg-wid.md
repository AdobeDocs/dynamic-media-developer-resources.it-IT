---
description: Larghezza visualizzazione. Specifica la larghezza dell’immagine di risposta (immagine di visualizzazione).
seo-description: Larghezza visualizzazione. Specifica la larghezza dell’immagine di risposta (immagine di visualizzazione).
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: b59b936c-abab-4f9d-95ca-0a09743ba0fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 4%

---


# wid{#wid}

Larghezza visualizzazione. Specifica la larghezza dell’immagine di risposta (immagine di visualizzazione).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Larghezza immagine in pixel (in numero maggiore di 0), </p></td> 
 </tr> 
</table>

## Predefinito {#section-830bae0b6bac440098444d7cdcb23e2e}

Se non vengono specificati né `wid=`, `hei=`, né `scale=`, l&#39;immagine di risposta corrisponde alla dimensione di visualizzazione predefinita specificata nel file FXG.

Il rendering dei formati raster viene eseguito utilizzando l&#39;impostazione Dimensione visualizzazione predefinita (o DefaultPix). Fate clic su **[!UICONTROL Impostazione applicazione]** > **[!UICONTROL Impostazione pubblicazione]** > **[!UICONTROL Server immagini]**, quindi immettete i valori di larghezza e altezza. Le dimensioni più ridotte garantiscono prestazioni migliori. Per applicare una modifica, dovete salvare le impostazioni ed eseguire una pubblicazione Image Server.

Se applicate un comando `scale=1`, viene eseguito il rendering di una richiesta di formato raster nelle dimensioni specificate nel file FXG.

## Esempio {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

A meno che non venga specificato un formato, l&#39;immagine viene rappresentata come file SWF. In questo caso, altezza e larghezza non hanno alcun significato, perché il file SWF in genere si espande fino alle dimensioni della finestra del browser. Di conseguenza, hei e wid si applicano solo ai formati raster o PDF. I formati raster includono:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha

