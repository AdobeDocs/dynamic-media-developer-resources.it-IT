---
description: IS fornisce meccanismi per semplificare l'uso delle mappe immagine HTML. Anche i visualizzatori basati su JAVA e basati su Flash in IS includono un supporto limitato per le mappe immagine.
solution: Experience Manager
title: Mappe immagine
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Mappe immagine{#image-maps}

IS fornisce meccanismi per semplificare l&#39;uso delle mappe immagine HTML. Anche i visualizzatori basati su JAVA e basati su Flash in IS includono un supporto limitato per le mappe immagine.

Le mappe immagine sorgente vengono fornite a IS tramite `catalog::Map` o con il comando `map=` e le mappe elaborate vengono recuperate utilizzando il comando `req=map`.

Una mappa immagine è costituita da uno o più elementi AREA HTML, correttamente delimitati con &#39;&lt;&#39; e &#39;>&#39;. Se fornito tramite catalog::Map, tutti i valori delle coordinate pixel si presume siano nella risoluzione dell&#39;immagine originale e relativi all&#39;angolo in alto a sinistra dell&#39;immagine sorgente (non modificata). Se viene fornito tramite un comando `map=`, i valori delle coordinate vengono considerati coordinate del livello, rispetto all&#39;angolo in alto a sinistra del livello (dopo `rotate=` e `extend=`).

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

Gli attributi `SHAPE` e `COORDS` di una `AREA` possono essere modificati durante l&#39;elaborazione di una richiesta `req=map`. Tutti gli altri attributi dell&#39;elemento `AREA` vengono passati senza modifiche. Nella maggior parte dei casi, questo comporta la modifica del valore `SHAPE` da `DEFAULT` a `RECT` (questo comporterebbe anche l&#39;aggiunta dell&#39;attributo `COORDS`) o la modifica dei valori `COORDS`.

Tutti gli elementi `AREA` che diventano vuoti durante l’elaborazione verranno rimossi del tutto. Se una mappa è associata a `layer=comp` viene posizionata dietro tutte le altre mappe. I dati vengono restituiti nel testo come uno o più elementi HTML `AREA`. Una stringa di risposta vuota indica che non esiste alcuna mappa immagine per gli oggetti specificati.

La trasparenza del livello non viene considerata per l’elaborazione delle mappe. A un livello completamente trasparente può ancora essere associata una mappa immagine. La mappa di un livello parzialmente trasparente non verrà ritagliata nelle aree trasparenti.

## Consultate anche {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ,  [catalogo::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), specifica  [HTML 4.01](http://www.w3.org/TR/html401/)
