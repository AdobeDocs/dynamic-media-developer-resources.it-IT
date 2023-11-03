---
description: IS fornisce meccanismi per semplificare l’utilizzo delle mappe immagine di HTML. I visualizzatori basati su JAVA e su Flash in IS includono anche il supporto limitato per le mappe immagine.
solution: Experience Manager
title: Mappe immagine
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Mappe immagine{#image-maps}

IS fornisce meccanismi per semplificare l’utilizzo delle mappe immagine di HTML. I visualizzatori basati su JAVA e su Flash in IS includono anche il supporto limitato per le mappe immagine.

Le mappe dell&#39;immagine sorgente vengono fornite a IS tramite `catalog::Map` o con `map=` e le mappe elaborate vengono recuperate utilizzando `req=map` comando.

Una mappa immagine è costituita da uno o più elementi HTML AREA, delimitati correttamente da &#39;&lt;&#39; e &#39;>&#39;. Se fornite tramite catalog::Map, si presume che tutti i valori delle coordinate in pixel siano nella risoluzione dell&#39;immagine originale e relativi all&#39;angolo superiore sinistro dell&#39;immagine sorgente (non modificata). Se fornito tramite una `map=` , i valori delle coordinate sono considerati coordinate di livello, rispetto all&#39;angolo superiore sinistro del livello (dopo `rotate=` e `extend=`).

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

Il `SHAPE` e `COORDS` attributi di un `AREA` possono essere modificati durante la trasformazione di un `req=map` richiesta, tutti gli altri attributi del `AREA` vengono passati senza modifiche. Nella maggior parte dei casi questo comporta la modifica del `SHAPE` valore da `DEFAULT` a `RECT` (questo aggiungerebbe anche il `COORDS` ), o la modifica del `COORDS` valori.

Qualsiasi `AREA` Gli elementi che diventano vuoti durante l’elaborazione vengono rimossi completamente. Se una mappa è associata a `layer=comp` è posizionato dietro tutte le altre mappe. I dati vengono restituiti sotto forma di testo come uno o più HTML `AREA` elementi. Una stringa di risposta vuota indica che non esiste alcuna mappa immagine per gli oggetti specificati.

La trasparenza dei livelli non viene considerata per l&#39;elaborazione delle mappe. A un livello completamente trasparente può essere ancora associata una mappa immagine. La mappa di un livello parzialmente trasparente non viene ritagliata nelle regioni trasparenti.

## Consultate anche {#see-also}

[map= mappa](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalogo::Mappa](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [Specifiche HTML 4.01](https://www.w3.org/TR/html401/)
