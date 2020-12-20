---
description: IS fornisce meccanismi per semplificare l’utilizzo di mappe immagine HTML. Anche i visualizzatori basati su JAVA e su Flash in IS includono un supporto limitato per le mappe immagine.
seo-description: IS fornisce meccanismi per semplificare l’utilizzo di mappe immagine HTML. Anche i visualizzatori basati su JAVA e su Flash in IS includono un supporto limitato per le mappe immagine.
seo-title: Mappe immagine
solution: Experience Manager
title: Mappe immagine
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---


# Mappe immagine{#image-maps}

IS fornisce meccanismi per semplificare l’utilizzo di mappe immagine HTML. Anche i visualizzatori basati su JAVA e su Flash in IS includono un supporto limitato per le mappe immagine.

Le mappe immagine sorgente vengono fornite a IS tramite `catalog::Map` o con il comando `map=`, e le mappe elaborate vengono recuperate utilizzando il comando `req=map`.

Una mappa immagine è costituita da uno o più elementi AREA HTML, delimitati correttamente da &#39;&lt;&#39; e &#39;>&#39;. Se fornito tramite catalogo::Map, si presume che tutti i valori delle coordinate pixel siano nella risoluzione immagine originale e relativi all’angolo in alto a sinistra dell’immagine sorgente (non modificata). Se viene fornito tramite un comando `map=`, si presume che i valori delle coordinate siano coordinate del livello, relative all&#39;angolo superiore sinistro del livello (dopo `rotate=` e `extend=`).

>[!NOTE]
>
>Al momento le coordinate % non sono consentite e possono essere elaborate in modo non corretto.

IS genera una mappa immagine composita dalle mappe immagine sorgente di ciascun livello costituente applicando le trasformazioni spaziali (come il ridimensionamento e la rotazione) alle coordinate della mappa, quindi assemblando le mappe dei livelli elaborati nell’ordine z appropriato (fronte retro) e con il posizionamento appropriato.

I comandi seguenti vengono considerati per l&#39;elaborazione delle mappe immagine quando vengono forniti insieme a `req=map` (direttamente nella richiesta, tramite modelli di catalogo o in `catalog::Modifier` stringhe):

* `align=`
* `wid=`
* `hei=`
* `scl=`
* `crop=`
* `flip=`
* `rotate=`
* `scale=`
* `layer=`
* `size=`
* `extend=`
* `origin=`
* `pos=`
* `anchor=`
* `src=`
* `map=`

Tutti gli altri comandi vengono ignorati.

Gli attributi `SHAPE` e `COORDS` di un elemento `AREA` possono essere modificati durante l&#39;elaborazione di una richiesta `req=map`. Tutti gli altri attributi dell&#39;elemento `AREA` vengono passati senza modifiche. Nella maggior parte dei casi, questo comporta la modifica del valore `SHAPE` da `DEFAULT` a `RECT` (in questo modo si aggiungerà anche l&#39;attributo `COORDS`) o i valori `COORDS`.

Tutti gli elementi `AREA` che diventano vuoti durante l&#39;elaborazione verranno rimossi completamente. Se una mappa è associata a `layer=comp` viene posizionata dietro tutte le altre mappe. I dati vengono restituiti nel testo come uno o più elementi HTML `AREA`. Una stringa di risposta vuota indica che non esiste alcuna mappa immagine per gli oggetti specificati.

La trasparenza del livello non viene considerata per l&#39;elaborazione delle mappe. A un livello completamente trasparente può ancora essere associata una mappa immagine. La mappa di un livello parzialmente trasparente non viene ritagliata alle aree trasparenti.

## Consultate anche {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ,  [catalogo::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), specifica  [HTML 4.01](http://www.w3.org/TR/html401/)
