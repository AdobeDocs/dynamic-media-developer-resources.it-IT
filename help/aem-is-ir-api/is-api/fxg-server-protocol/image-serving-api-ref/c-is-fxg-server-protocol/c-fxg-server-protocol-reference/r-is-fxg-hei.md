---
title: hei
description: Altezza visualizzazione. Specifica l'altezza dell'immagine di risposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
TQID: 'https://experienceleague.adobe.com/Tpl8zVXQVzs3isa26A3YvnOzs6gqpz3-4L-qDBx-eK0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 174
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
