---
description: Image Server supporta file SVG (Scalable Vector Graphics) come dati sorgente. È richiesta la conformità a SVG 1.1.
solution: Experience Manager
title: Supporto SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Supporto SVG{#svg-support}

Image Server supporta file SVG (Scalable Vector Graphics) come dati sorgente. È richiesta la conformità a SVG 1.1.

Image Server riconosce solo i contenuti SVG statici; non sono supportate animazioni, script e altri contenuti interattivi.

È possibile specificare SVG ovunque siano consentiti i file di immagine (percorso URL, `src=` e `mask=`). Dopo la rasterizzazione del contenuto del file SVG, questo viene gestito come un’immagine.

Analogamente alle immagini, i file SVG possono essere specificati come voci del catalogo immagini o come percorsi di file relativi.

## Variabili di sostituzione {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` variabili di sostituzione possono essere incluse nel file SVG nelle stringhe di valore `<text>` elementi e in qualsiasi attributo di elemento.

Le variabili importanti nella porzione query delle richieste Image Server incorporate non vengono sostituite direttamente. Piuttosto, tutte le definizioni di variabili disponibili vengono aggiunte alla richiesta, consentendo al server immagini di sostituire le variabili durante l’analisi della richiesta.

Per ulteriori informazioni, vedere [Variabili di sostituzione](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a).

## Riferimenti immagine {#section-a7680f9e6aca4b1a83560637cc9fac66}

Le immagini possono essere inserite in SVG utilizzando l&#39;elemento `<image>`. Le immagini a cui fa riferimento l&#39;attributo `xlink::href` dell&#39;elemento `<image>` devono essere richieste di server immagini valide. Gli URL esterni non sono consentiti.

Specificare una richiesta completa di Image Server, a partire da `http://`, oppure un URL relativo, a partire da `/is/image`. Se viene specificato un percorso HTTP completo, il nome di dominio viene rimosso dal percorso per essere convertito nel formato relativo. L’utilizzo di un percorso HTTP completo può essere utile, in quanto consente di visualizzare l’anteprima del file con un renderer SVG di terze parti.

>[!NOTE]
>
>Il supporto per il rendering delle immagini in questa versione di Image Server è limitato. Le immagini di riferimento provenienti da SVG devono essere utilizzate solo in situazioni in cui i tradizionali meccanismi di creazione di modelli e livelli di Image Server non sono sufficienti per ottenere il risultato desiderato. In nessun caso SVG deve essere utilizzato per generare composizioni con più immagini.

>[!NOTE]
>
>Le immagini incorporate in SVG non vengono ridimensionate automaticamente in questo momento. Assicurarsi che tutti i riferimenti immagine includano i comandi Image Server necessari per impostare la dimensione immagine desiderata (ad esempio, `wid=`). Se la dimensione dell&#39;immagine non è impostata in modo esplicito, viene applicato `attribute::DefaultPix`.

## Gestione colore {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Si presume che tutti i valori di colore incorporati nei file SVG e passati ai modelli SVG tramite variabili di sostituzione siano presenti nello spazio colore `sRgb`.

Non viene eseguita alcuna conversione del colore quando le immagini sono incorporate nel SVG. Per garantire la fedeltà dei colori, assicurarsi di specificare `icc=sRgb` per tutte le richieste di immagini incorporate.

Dopo la rasterizzazione, l&#39;immagine SVG partecipa alla gestione del colore come qualsiasi altra immagine.

## Esempio {#section-036cdd45abd449849ee00a8f21788c28}

Il seguente modello di SVG illustra i riferimenti alle immagini e l’utilizzo di variabili.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Questo modello di SVG può essere utilizzato come segue:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrizioni {#section-daa5eccd07204aaf993be41e87822d54}

I file SVG devono essere autonomi e non devono fare riferimento a file o risorse secondari, ad eccezione delle immagini esterne a cui si fa riferimento nelle richieste di Image Server o Image Rendering (vedi sopra).

Viene eseguito il rendering solo del contenuto statico. Animazione, funzioni interattive, ad esempio pulsanti e così via. può essere presente ma non essere visualizzato come previsto.

Al momento non sono supportate specifiche colore basate sul profilo ICC.

`<script>` elementi potrebbero essere presenti ma vengono sempre ignorati.

## Consultate anche {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Specifica di SVG 1.1](https://www.w3.org/TR/SVG11/)
