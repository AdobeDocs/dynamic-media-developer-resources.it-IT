---
description: IS fornisce meccanismi per semplificare l’utilizzo delle mappe immagine di HTML. Anche i visualizzatori basati su JAVA e basati su Flash in IS includono un supporto limitato per le mappe immagine.
solution: Experience Manager
title: Mappe immagine
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Mappe immagine{#image-maps}

IS fornisce meccanismi per semplificare l’utilizzo delle mappe immagine di HTML. Anche i visualizzatori basati su JAVA e basati su Flash in IS includono un supporto limitato per le mappe immagine.

Le mappe immagine sorgente vengono fornite a IS tramite `catalog::Map` o con `map=` e le mappe elaborate vengono recuperate utilizzando `req=map` comando.

Una mappa immagine è costituita da uno o più elementi AREA di HTML, delimitati correttamente con &quot;&lt;&quot; e &quot;>&quot;. Se fornito tramite catalog::Map, tutti i valori delle coordinate pixel si presume siano nella risoluzione dell&#39;immagine originale e relativi all&#39;angolo in alto a sinistra dell&#39;immagine sorgente (non modificata). Quando viene fornito tramite un `map=` i valori delle coordinate sono considerati coordinate del livello, rispetto all&#39;angolo superiore sinistro del livello (dopo `rotate=` e `extend=`).

>[!NOTE]
>
>Al momento le coordinate % non sono consentite e possono essere elaborate in modo errato.

IS genera una mappa immagine composita dalle mappe immagine sorgente di ciascun livello costituente applicando le trasformazioni spaziali (come la scala e la rotazione) alle coordinate della mappa, quindi assemblando le mappe dei livelli elaborati nell&#39;ordine z appropriato (da anteriore a posteriore) e con il posizionamento appropriato.

I seguenti comandi vengono considerati per l’elaborazione della mappa immagine quando vengono forniti insieme a `req=map` (direttamente nella richiesta, tramite modelli di catalogo o in `catalog::Modifier` stringhe):

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

La `SHAPE` e `COORDS` attributi di un `AREA` possono essere modificate durante la trasformazione di un `req=map` richiesta, tutti gli altri attributi del `AREA` vengono passati senza modifiche. Nella maggior parte dei casi, si tratta di modificare il `SHAPE` valore da `DEFAULT` a `RECT` (questo aggiungerebbe anche la `COORDS` (attributo), o la modifica del `COORDS` valori.

Qualsiasi `AREA` gli elementi che diventano vuoti durante l’elaborazione vengono rimossi completamente. Se una mappa è associata a `layer=comp` è posto dietro tutte le altre mappe. I dati vengono restituiti sotto forma di testo come o più HTML `AREA` elementi. Una stringa di risposta vuota indica che non esiste alcuna mappa immagine per gli oggetti specificati.

La trasparenza del livello non viene considerata per l’elaborazione delle mappe. A un livello completamente trasparente può ancora essere associata una mappa immagine. La mappa di un livello parzialmente trasparente non verrà ritagliata nelle aree trasparenti.

## Consultate anche {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalogo::Mappa](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [Specifiche di HTML 4.01](https://www.w3.org/TR/html401/)
