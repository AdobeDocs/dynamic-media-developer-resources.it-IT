---
title: wid
description: Larghezza visualizzazione. Specifica la larghezza dell'immagine di risposta (immagine di visualizzazione).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
TQID: 'https://experienceleague.adobe.com/A1n6WpZEsDWfdLoQZZY-ykX4zXjG86BRXHnVfcpO9yo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 176
ht-degree: 1%

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

Se non vengono specificati né `wid=`, `hei=`, né `scale=`, l&#39;immagine di risposta corrisponde alle dimensioni di visualizzazione predefinite specificate nel file FXG.

Il rendering dei formati raster viene eseguito utilizzando l&#39;impostazione Default View Size (o DefaultPix). Fai clic su **[!UICONTROL Impostazione applicazione]** > **[!UICONTROL Impostazione pubblicazione]** > **[!UICONTROL Server immagini]**, quindi immetti i valori di larghezza e altezza. Le dimensioni più piccole offrono prestazioni migliori. Salva le impostazioni ed esegui una pubblicazione Image Server per applicare una modifica.

Se si applica un comando `scale=1`, viene eseguito il rendering di una richiesta in formato raster alle dimensioni specificate in FXG.

## Esempio {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

A meno che non sia specificato un formato, l&#39;immagine viene riprodotta come file SWF. In questo caso, l’altezza e la larghezza non hanno alcun significato, perché SWF in genere si espande alle dimensioni della finestra del browser. Di conseguenza, `hei` e `wid` si applicano solo ai formati raster o PDF. I formati raster includono:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa
