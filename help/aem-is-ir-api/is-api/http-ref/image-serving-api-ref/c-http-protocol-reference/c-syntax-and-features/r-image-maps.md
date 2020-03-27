---
description: IS fornisce meccanismi per semplificare l’utilizzo di mappe immagine HTML. I visualizzatori basati su JAVA e su Flash presenti in IS includono anche un supporto limitato per le mappe immagine.
seo-description: IS fornisce meccanismi per semplificare l’utilizzo di mappe immagine HTML. I visualizzatori basati su JAVA e su Flash presenti in IS includono anche un supporto limitato per le mappe immagine.
seo-title: Mappe immagine
solution: Experience Manager
title: Mappe immagine
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# Image maps{#image-maps}

IS fornisce meccanismi per semplificare l’utilizzo di mappe immagine HTML. I visualizzatori basati su JAVA e su Flash presenti in IS includono anche un supporto limitato per le mappe immagine.

Le mappe immagine sorgente vengono fornite a IS tramite `catalog::Map` o con il `map=` comando, e le mappe elaborate vengono recuperate utilizzando il `req=map` comando.

Una mappa immagine è costituita da uno o più elementi AREA HTML, delimitati correttamente da &#39;&lt;&#39; e &#39;>&#39;. Se fornito tramite catalogo::Map, si presume che tutti i valori delle coordinate pixel siano nella risoluzione immagine originale e siano relativi all’angolo in alto a sinistra dell’immagine sorgente (non modificata). Se viene fornito tramite un `map=` comando, si presume che i valori delle coordinate siano coordinate del livello, relative all’angolo superiore sinistro del livello (dopo `rotate=` e `extend=`).

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Al momento le coordinate % non sono consentite e possono essere elaborate in modo non corretto.

IS genera una mappa immagine composita dalle mappe immagine sorgente di ciascun livello costituente applicando le trasformazioni spaziali (come il ridimensionamento e la rotazione) alle coordinate della mappa, quindi assemblando le mappe dei livelli elaborati nell’ordine z appropriato (fronte retro) e con il posizionamento appropriato.

I comandi seguenti sono considerati per l’elaborazione delle mappe immagine quando vengono forniti insieme `req=map` (direttamente nella richiesta, tramite modelli di catalogo o in `catalog::Modifier` stringhe):

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

Gli `SHAPE` attributi e `COORDS` gli attributi di un `AREA` elemento possono essere modificati durante l&#39;elaborazione di una `req=map` richiesta, tutti gli altri attributi dell&#39; `AREA` elemento vengono passati senza modifiche. Nella maggior parte dei casi, questo comporta la modifica del `SHAPE` valore da `DEFAULT` a `RECT` (in questo modo si aggiungerà anche l’ `COORDS` attributo) o la modifica dei `COORDS` valori.

Tutti `AREA` gli elementi che diventano vuoti durante l&#39;elaborazione verranno rimossi completamente. Se una mappa è associata ad essa `layer=comp` viene posizionata dietro tutte le altre mappe. I dati vengono restituiti nel testo come uno o più `AREA` elementi HTML. Una stringa di risposta vuota indica che non esiste alcuna mappa immagine per gli oggetti specificati.

La trasparenza del livello non viene considerata per l&#39;elaborazione delle mappe. A un livello completamente trasparente può ancora essere associata una mappa immagine. La mappa di un livello parzialmente trasparente non viene ritagliata alle aree trasparenti.

## Consultate anche {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalogo::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), specifica [HTML 4.01](http://www.w3.org/TR/html401/)
