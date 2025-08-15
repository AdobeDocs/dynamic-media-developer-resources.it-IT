---
description: IS fornisce meccanismi per semplificare l'utilizzo delle mappe immagine di HTML. I visualizzatori basati su JAVA e Flash in IS includono anche il supporto limitato per le mappe immagine.
solution: Experience Manager
title: Mappe immagine
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Mappe immagine{#image-maps}

IS fornisce meccanismi per semplificare l&#39;utilizzo delle mappe immagine di HTML. I visualizzatori basati su JAVA e Flash in IS includono anche il supporto limitato per le mappe immagine.

Le mappe immagine di Source vengono fornite a IS tramite `catalog::Map` o con il comando `map=` e le mappe elaborate vengono recuperate utilizzando il comando `req=map`.

Una mappa immagine è costituita da uno o più elementi HTML AREA, delimitati correttamente da &quot;&lt;&quot; e &quot;>&quot;. Se fornite tramite catalog::Map, si presume che tutti i valori delle coordinate in pixel siano nella risoluzione dell&#39;immagine originale e relativi all&#39;angolo superiore sinistro dell&#39;immagine sorgente (non modificata). Se fornite tramite un comando `map=`, i valori delle coordinate vengono considerati come coordinate di livello, relative all&#39;angolo superiore sinistro del livello (dopo `rotate=` e `extend=`).

>[!NOTE]
>
>Le coordinate % non sono attualmente consentite e potrebbero essere elaborate in modo errato.

IS genera una mappa immagine composita dalle mappe dell&#39;immagine sorgente di ciascun livello costitutivo applicando le trasformazioni spaziali (come la scalabilità e la rotazione) alle coordinate della mappa, quindi assemblando le mappe del livello elaborate nell&#39;ordine z appropriato (da davanti a dietro) e con il posizionamento appropriato.

I seguenti comandi vengono considerati per l&#39;elaborazione della mappa immagine se forniti insieme a `req=map` (direttamente nella richiesta, tramite modelli di catalogo o in `catalog::Modifier` stringhe):

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

Tutti gli altri comandi vengono effettivamente ignorati.

Gli attributi `SHAPE` e `COORDS` di un `AREA` possono essere modificati durante l&#39;elaborazione di una richiesta `req=map`. Tutti gli altri attributi dell&#39;elemento `AREA` vengono passati senza modifiche. Nella maggior parte dei casi, questo comporta la modifica del valore `SHAPE` da `DEFAULT` a `RECT` (con l&#39;aggiunta dell&#39;attributo `COORDS`) o la modifica dei valori `COORDS`.

Tutti gli elementi `AREA` che diventano vuoti durante l&#39;elaborazione vengono rimossi completamente. Se una mappa è associata a `layer=comp`, viene posizionata dietro tutte le altre mappe. I dati vengono restituiti come uno o più elementi di HTML `AREA`. Una stringa di risposta vuota indica che non esiste alcuna mappa immagine per gli oggetti specificati.

La trasparenza dei livelli non viene considerata per l&#39;elaborazione delle mappe. A un livello completamente trasparente può essere ancora associata una mappa immagine. La mappa di un livello parzialmente trasparente non viene ritagliata nelle regioni trasparenti.

## Consultate anche {#see-also}

[mappa=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalogo::mappa](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [specifica di HTML 4.01](https://www.w3.org/TR/html401/)
