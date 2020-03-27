---
description: Altezza visualizzazione. Specifica l'altezza dell'immagine di risposta.
seo-description: Altezza visualizzazione. Specifica l'altezza dell'immagine di risposta.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f7e580b-6399-4661-b5d9-8044574ba124
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

Il rendering dei formati raster viene eseguito utilizzando l&#39;impostazione Dimensione visualizzazione predefinita (o DefaultPix). Fate clic su **[!UICONTROL Impostazione]** applicazione > Impostazione **** pubblicazione > Server **** immagini, quindi immettete i valori di larghezza e altezza. Le dimensioni più ridotte garantiscono prestazioni migliori. Per applicare una modifica, dovete salvare le impostazioni ed eseguire una pubblicazione Image Server.

Se applicate un `scale=1` comando, viene eseguito il rendering di una richiesta di formato raster nelle dimensioni specificate nel file FXG.

## Predefinito {#section-76ee3daa77cb468ab310821357cc9404}

Se non `wid=`, `hei=`né `scale=` vengono specificati, l&#39;immagine di risposta corrisponde alla dimensione di visualizzazione predefinita specificata nel file FXG.

## Esempio {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

A meno che non venga specificato un formato, l&#39;immagine viene rappresentata come file SWF. In questo caso, altezza e larghezza non hanno alcun significato, perché il file SWF in genere si espande fino alle dimensioni della finestra del browser. Di conseguenza, hei e wid si applicano solo ai formati raster o PDF. I formati raster includono:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha

