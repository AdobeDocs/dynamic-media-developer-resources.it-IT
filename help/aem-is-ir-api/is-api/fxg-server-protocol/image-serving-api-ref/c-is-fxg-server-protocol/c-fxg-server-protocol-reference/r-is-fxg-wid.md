---
description: Larghezza visualizzazione. Specifica la larghezza dell'immagine di risposta (visualizza immagine).
seo-description: Larghezza visualizzazione. Specifica la larghezza dell'immagine di risposta (visualizza immagine).
seo-title: wid
solution: Experience Manager
title: nudo
uuid: b59b936c-abab-4f9d-95ca-0a09743ba0fb
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 4%

---


# wid{#wid}

Larghezza visualizzazione. Specifica la larghezza dell&#39;immagine di risposta (visualizza immagine).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Larghezza immagine in pixel (in numero maggiore di 0), </p></td> 
 </tr> 
</table>

## Predefinito {#section-830bae0b6bac440098444d7cdcb23e2e}

Se non vengono specificati né `wid=`, `hei=`, né `scale=`, l&#39;immagine di risposta corrisponde alla dimensione di visualizzazione predefinita specificata nel file FXG.

Il rendering dei formati raster viene eseguito utilizzando la dimensione di visualizzazione predefinita (o l&#39;impostazione DefaultPix). Fai clic su **[!UICONTROL Impostazione applicazione]** > **[!UICONTROL Impostazioni pubblicazione]** > **[!UICONTROL Image Server]**, quindi immetti i valori di Larghezza e Altezza. Le dimensioni più piccole offrono prestazioni migliori. Per applicare una modifica, è necessario salvare le impostazioni ed eseguire una pubblicazione di Image Server.

Se si applica un comando `scale=1`, viene eseguito il rendering di una richiesta di formato raster nelle dimensioni specificate nell&#39;FXG.

## Esempio {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

A meno che non venga specificato un formato, l&#39;immagine viene riprodotta come file SWF. In questo caso, altezza e larghezza non hanno alcun significato, perché il SWF di solito si espande fino alle dimensioni della finestra del browser. Di conseguenza, hei e wid si applicano solo ai formati raster o PDF. I formati raster includono:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alpha

