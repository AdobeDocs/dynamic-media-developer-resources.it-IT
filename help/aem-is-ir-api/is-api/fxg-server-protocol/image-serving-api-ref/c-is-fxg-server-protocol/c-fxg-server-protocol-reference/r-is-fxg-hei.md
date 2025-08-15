---
title: hei
description: Altezza visualizzazione. Specifica l'altezza dell'immagine di risposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# hei{#hei}

Altezza visualizzazione. Specifica l&#39;altezza dell&#39;immagine di risposta.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Altezza immagine in pixel (int maggiore di 0). </p></td> 
 </tr> 
</table>

Il rendering dei formati raster viene eseguito utilizzando l&#39;impostazione Default View Size (o DefaultPix). Seleziona **[!UICONTROL Impostazione applicazione]** > **[!UICONTROL Impostazione pubblicazione]** > **[!UICONTROL Server immagini]**, quindi immetti i valori di larghezza e altezza. Le dimensioni più piccole offrono prestazioni migliori. Salva le impostazioni ed esegui una pubblicazione Image Server per applicare una modifica.

Se si applica un comando `scale=1`, viene eseguito il rendering di una richiesta in formato raster alle dimensioni specificate in FXG.

## Predefinito {#section-76ee3daa77cb468ab310821357cc9404}

Se `wid=`, `hei=` o `scale=` non sono specificati, l&#39;immagine di risposta è la dimensione di visualizzazione predefinita specificata nel file FXG.

## Esempio {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

A meno che non sia specificato un formato, l&#39;immagine viene riprodotta come file SWF. In questo caso, l’altezza e la larghezza non hanno alcun significato, perché SWF in genere si espande alle dimensioni della finestra del browser. Di conseguenza, hei e wid si applicano solo ai formati raster o PDF. I formati raster includono:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa
