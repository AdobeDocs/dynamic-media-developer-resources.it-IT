---
description: Image Serving supporta file SVG (Scalable Vector Graphics) come dati di origine. È richiesta la conformità a SVG 1.1.
solution: Experience Manager
title: Supporto SVG
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Supporto SVG{#svg-support}

Image Serving supporta file SVG (Scalable Vector Graphics) come dati di origine. È richiesta la conformità a SVG 1.1.

Image Serving riconosce solo i contenuti statici SVG; animazioni, script e altri contenuti interattivi non sono supportati.

È possibile specificare SVG ovunque siano consentiti i file immagine (percorso URL, `src=` e `mask=`). Una volta rasterizzato il contenuto del file SVG, questo viene gestito come un’immagine.

Analogamente alle immagini, i file SVG possono essere specificati come voci di catalogo immagini o come percorsi di file relativi.

## Variabili di sostituzione {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` le variabili di sostituzione possono essere incluse nel file SVG negli  `<text>` elementi delle stringhe di valore e in qualsiasi attributo di elemento.

Le variabili importanti nella sezione query delle richieste incorporate di Image Serving non vengono sostituite direttamente. Al contrario, tutte le definizioni di variabili disponibili vengono aggiunte alla richiesta, il che consente a Image Serving di sostituire le variabili quando la richiesta viene analizzata.

Per ulteriori informazioni, consulta [Variabili di sostituzione](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) .

## Riferimenti immagine {#section-a7680f9e6aca4b1a83560637cc9fac66}

Le immagini possono essere inserite in SVG utilizzando l’elemento `<image>` . Le immagini a cui fa riferimento l&#39;attributo `xlink::href` dell&#39;elemento `<image>` devono essere richieste di servizio immagini valide. Gli URL esterni non sono consentiti.

Specifica una richiesta completa di Image Server, a partire da `http://`, o un URL relativo, a partire da `/is/image`. Se viene specificato un percorso HTTP completo, il nome di dominio verrà rimosso dal percorso per la conversione nel formato relativo. L’utilizzo di un percorso HTTP completo potrebbe risultare vantaggioso, in quanto consente l’anteprima del file con un modulo di rendering SVG di terze parti.

>[!NOTE]
>
>Il supporto per il rendering delle immagini in questa versione di Image Serving è limitato. Le immagini di riferimento provenienti da SVG devono essere utilizzate solo in situazioni in cui i meccanismi tradizionali di modellazione e stratificazione di Image Serving non sono sufficienti per ottenere il risultato desiderato. In nessun caso SVG deve essere utilizzato per generare compositi con più immagini.

>[!NOTE]
>
>Al momento le immagini incorporate in SVG non vengono ridimensionate automaticamente. Assicurati che tutti gli hrefs dell&#39;immagine includano i comandi Image Serving necessari per impostare le dimensioni dell&#39;immagine desiderate (ad esempio `wid=`). Se le dimensioni dell’immagine non sono impostate esplicitamente, verrà applicato `attribute::DefaultPix`.

## Gestione del colore {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Tutti i valori di colore incorporati nei file SVG e passati ai modelli SVG tramite variabili di sostituzione si presumono presenti nello spazio di colore `sRgb`.

Non viene eseguita alcuna conversione del colore quando le immagini sono incorporate nell’SVG. Per garantire la fedeltà del colore, assicurati di specificare `icc=sRgb` per tutte le richieste di immagini incorporate.

Dopo la rasterizzazione, l&#39;immagine SVG partecipa alla gestione del colore come qualsiasi altra immagine.

## Esempio {#section-036cdd45abd449849ee00a8f21788c28}

Il seguente modello SVG illustra i riferimenti alle immagini e l’uso delle variabili.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Questo modello SVG può essere utilizzato come segue:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrizioni {#section-daa5eccd07204aaf993be41e87822d54}

I file SVG devono essere autonomi e non devono fare riferimento a file o risorse secondari, ad eccezione delle immagini esterne a cui si fa riferimento con le richieste Image Server o Image Rendering (vedi sopra).

Viene eseguito il rendering solo del contenuto statico. Animazione, funzioni interattive, come pulsanti, ecc. può essere presente ma non può essere reso come previsto.

Le specifiche dei colori basate sul profilo ICC non sono al momento supportate.

`<script>` gli elementi possono essere presenti ma vengono sempre ignorati.

## Consultate anche {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), specifica  [SVG 1.1](http://www.w3.org/TR/SVG11/)
