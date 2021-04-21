---
description: Altezza visualizzazione. Specifica l'altezza dell'immagine di risposta.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 3%

---


# hei{#hei}

Altezza visualizzazione. Specifica l&#39;altezza dell&#39;immagine di risposta.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Altezza immagine in pixel (in numero maggiore di 0). </p></td> 
 </tr> 
</table>

Il rendering dei formati raster viene eseguito utilizzando la dimensione di visualizzazione predefinita (o l&#39;impostazione DefaultPix). Fai clic su **[!UICONTROL Impostazione applicazione]** > **[!UICONTROL Impostazioni pubblicazione]** > **[!UICONTROL Image Server]**, quindi immetti i valori di Larghezza e Altezza. Le dimensioni più piccole offrono prestazioni migliori. Per applicare una modifica, è necessario salvare le impostazioni ed eseguire una pubblicazione di Image Server.

Se si applica un comando `scale=1`, viene eseguito il rendering di una richiesta di formato raster nelle dimensioni specificate nell&#39;FXG.

## Predefinito {#section-76ee3daa77cb468ab310821357cc9404}

Se non vengono specificati né `wid=`, `hei=`, né `scale=`, l&#39;immagine di risposta corrisponde alla dimensione di visualizzazione predefinita specificata nel file FXG.

## Esempio {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

A meno che non venga specificato un formato, l&#39;immagine viene riprodotta come file SWF. In questo caso, altezza e larghezza non hanno alcun significato, perché il SWF di solito si espande fino alle dimensioni della finestra del browser. Di conseguenza, hei e wid si applicano solo ai formati raster o PDF. I formati raster includono:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alpha

