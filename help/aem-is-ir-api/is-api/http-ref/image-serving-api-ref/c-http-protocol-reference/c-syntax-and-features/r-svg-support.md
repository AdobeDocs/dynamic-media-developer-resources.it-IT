---
description: Image Serving supporta file SVG (Scalable Vector Graphics) come dati sorgente. È richiesta la conformità con SVG 1.1.
seo-description: Image Serving supporta file SVG (Scalable Vector Graphics) come dati sorgente. È richiesta la conformità con SVG 1.1.
seo-title: Supporto SVG
solution: Experience Manager
title: Supporto SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: 30d7b37d-fdef-4518-a4b3-4baee56fa634
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Supporto SVG{#svg-support}

Image Serving supporta file SVG (Scalable Vector Graphics) come dati sorgente. È richiesta la conformità con SVG 1.1.

Image Serving riconosce solo i contenuti SVG statici; animazioni, script e altri contenuti interattivi non sono supportati.

SVG può essere specificato ovunque siano consentiti i file immagine (percorso URL `src=`, e `mask=`). Una volta rasterizzato il contenuto del file SVG, questo viene gestito come un’immagine.

Come per le immagini, i file SVG possono essere specificati come voci di catalogo immagini o come percorsi di file relativi.

## Variabili di sostituzione {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` le variabili di sostituzione possono essere incluse nel file SVG negli `<text>` elementi stringa valore e in qualsiasi attributo di elemento.

Le variabili importanti nella parte query delle richieste Image Server incorporate non vengono sostituite direttamente. Al contrario, alla richiesta vengono aggiunte tutte le definizioni di variabili disponibili, che consentono a Image Server di sostituire le variabili durante l’analisi della richiesta.

Per ulteriori informazioni, vedere Variabili [di](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) sostituzione.

## Riferimenti immagine {#section-a7680f9e6aca4b1a83560637cc9fac66}

Le immagini possono essere inserite in SVG utilizzando l’ `<image>` elemento . Le immagini a cui fa riferimento l&#39; `xlink::href` attributo dell&#39; `<image>` elemento devono essere richieste di trasmissione di immagini valide. Gli URL esterni non sono consentiti.

Specificate una richiesta di Image Server completa, a partire da `http://`o un URL relativo, a partire da `/is/image`. Se viene specificato un percorso HTTP completo, il nome del dominio verrà rimosso dal percorso per la conversione al formato relativo. L&#39;utilizzo di un percorso HTTP completo potrebbe risultare vantaggioso, in quanto consente l&#39;anteprima del file con un renderer SVG di terze parti.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Il supporto per il rendering delle immagini in questa versione di Image Server è limitato. Le immagini di riferimento provenienti da SVG devono essere utilizzate solo in situazioni in cui i tradizionali meccanismi di generazione dei livelli e di tempiazione di Image Server non sono sufficienti per ottenere il risultato desiderato. In nessun caso è consigliabile usare SVG per generare composizioni con più immagini.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Al momento, le immagini incorporate in SVG non vengono ridimensionate automaticamente. Accertatevi che tutti gli scaffali delle immagini includano i comandi Image Serving necessari per impostare le dimensioni desiderate (ad es. `wid=`). Se le dimensioni dell&#39;immagine non sono impostate in modo esplicito, `attribute::DefaultPix` verranno applicate.

## Color management {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Tutti i valori di colore incorporati nei file SVG e passati ai modelli SVG tramite variabili di sostituzione si presume siano presenti nello spazio `sRgb` colore.

Non viene eseguita alcuna conversione del colore quando le immagini vengono incorporate nel file SVG. Per garantire la fedeltà dei colori, accertatevi di specificare `icc=sRgb` per tutte le richieste di immagini incorporate.

Dopo la rasterizzazione, l&#39;immagine SVG partecipa alla gestione del colore come qualsiasi altra immagine.

## Esempio {#section-036cdd45abd449849ee00a8f21788c28}

Il seguente modello SVG illustra i riferimenti immagine e l’utilizzo di variabili.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Questo modello SVG può essere utilizzato come segue:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrizioni {#section-daa5eccd07204aaf993be41e87822d54}

I file SVG devono essere indipendenti e non devono fare riferimento ad alcun file o risorsa secondario, ad eccezione delle immagini esterne a cui si fa riferimento con le richieste Image Server o Image Rendering (vedi sopra).

Viene eseguito il rendering solo del contenuto statico. Animazione, funzioni interattive, come pulsanti, ecc. può essere presente ma non può essere rappresentato come previsto.

Al momento non sono supportate le specifiche di colore basate sul profilo ICC.

`<script>` gli elementi possono essere presenti ma vengono sempre ignorati.

## Consultate anche {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), specifica [SVG 1.1](http://www.w3.org/TR/SVG11/)
