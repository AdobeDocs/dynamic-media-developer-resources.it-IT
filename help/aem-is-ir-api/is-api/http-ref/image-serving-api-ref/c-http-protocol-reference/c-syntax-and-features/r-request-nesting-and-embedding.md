---
description: Image Serving supporta la nidificazione illimitata delle richieste Image Server, l’incorporazione delle richieste di rendering delle immagini e l’incorporazione delle immagini recuperate dai server esteri. Questi meccanismi sono supportati solo dalle immagini dei livelli e dalle maschere di livello.
seo-description: Image Serving supporta la nidificazione illimitata delle richieste Image Server, l’incorporazione delle richieste di rendering delle immagini e l’incorporazione delle immagini recuperate dai server esteri. Questi meccanismi sono supportati solo dalle immagini dei livelli e dalle maschere di livello.
seo-title: Richiesta di nidificazione e incorporazione
solution: Experience Manager
title: Richiesta di nidificazione e incorporazione
topic: Scene7 Image Serving - Image Rendering API
uuid: 59031329-e65f-4631-bc7d-83f2540cc836
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '1075'
ht-degree: 0%

---


# Richiesta di nidificazione e incorporazione{#request-nesting-and-embedding}

Image Serving supporta la nidificazione illimitata delle richieste Image Server, l’incorporazione delle richieste di rendering delle immagini e l’incorporazione delle immagini recuperate dai server esteri. Questi meccanismi sono supportati solo dalle immagini dei livelli e dalle maschere di livello.

>[!NOTE]
>
>Alcuni client e server proxy e-mail possono codificare le parentesi graffe utilizzate per la sintassi di nidificazione e di incorporamento. Le applicazioni per le quali si tratta di un problema devono utilizzare le parentesi al posto delle parentesi graffe.

## Richieste Image Server nidificate {#section-6954202119e0466f8ff27c79f4f039c8}

Un’intera richiesta Image Server può essere usata come sorgente del livello specificandola nel comando `src=` (o `mask=`) con la sintassi seguente:

`…&src=is( nestedRequest)&…`

Il token `is` fa distinzione tra maiuscole e minuscole.

La richiesta nidificata non deve includere il percorso principale del server (in genere ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>I caratteri di delimitazione delle richieste nidificati ( `'(',')'`) e i caratteri di delimitazione dei comandi ( `'?'`, `'&'`, `'='`) all&#39;interno delle richieste nidificate non devono essere codificati per HTTP. In effetti, le richieste nidificate devono essere codificate come la richiesta esterna (nidificazione).

Le regole di pre-elaborazione vengono applicate alle richieste nidificate.

I comandi seguenti vengono ignorati quando specificati in richieste nidificate (nell&#39;URL della richiesta o in `catalog::Modifier` o `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Se l&#39;immagine del risultato delle richieste nidificate include dati di maschera (alfa), viene passata al livello di incorporamento come maschera di livello.

Vengono inoltre ignorati `attribute::MaxPix`e `attribute::DefaultPix` del catalogo immagini applicato alla richiesta nidificata.

Il risultato dell&#39;immagine di una richiesta IS nidificata può essere memorizzato nella cache facoltativamente includendo `cache=on`. Per impostazione predefinita, il caching dei dati intermedi è disattivato. La memorizzazione nella cache deve essere abilitata solo quando è previsto che l&#39;immagine intermedia venga riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. È applicabile la gestione standard della cache lato server. I dati vengono memorizzati nella cache in un formato senza perdita di dati.

## Richieste di rendering immagini incorporate {#section-69c5548db930412b9b90d9b2951a6969}

Quando Scene7 Image Rendering è abilitato sul server, le richieste di rendering possono essere utilizzate come origini di livello specificandole nel comando src= (o mask=). Utilizzate la sintassi seguente:

` …&src=ir( *[!DNL renderRequest]*)&…`

Il token `ir` fa distinzione tra maiuscole e minuscole.

*[!DNL renderRequest]* è la normale richiesta di rendering delle immagini, escluso il percorso principale HTTP  ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>I caratteri di delimitazione delle richieste nidificati ( `'(',')'`) e i caratteri di delimitazione dei comandi ( `'?'`, `'&'`, `'='`) all&#39;interno delle richieste nidificate non devono essere codificati per HTTP. In effetti, le richieste incorporate devono essere codificate come la richiesta esterna (incorporazione).

I seguenti comandi Image Rendering vengono ignorati quando specificati in richieste nidificate:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Vengono inoltre ignorati `attribute::MaxPix` e `attribute::DefaultPix` del catalogo di materiali applicabile alla richiesta di rendering nidificata.

Il risultato dell&#39;immagine di una richiesta IR nidificata può essere memorizzato nella cache facoltativamente includendo `cache=on`. Per impostazione predefinita, il caching dei dati intermedi è disattivato. La memorizzazione nella cache deve essere abilitata solo quando è previsto che l&#39;immagine intermedia venga riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. È applicabile la gestione standard della cache lato server. I dati vengono memorizzati nella cache in un formato senza perdita di dati.

## Richieste di rendering FXG incorporate {#section-c817e4b4f7da414ea5a51252ca7e120a}

Quando il renderer grafico FXG (alias [!DNL AGMServer]) è installato e attivato con Image Server, le richieste FXG possono essere utilizzate come sorgenti di livello specificandole nei comandi `src=` (o `mask=`). Utilizzate la sintassi seguente:

`…&src=fxg( renderRequest)&…`

Il token `fxg` fa distinzione tra maiuscole e minuscole.

>[!NOTE]
>
>Il rendering di elementi grafici FXG è disponibile solo nell&#39;ambiente ospitato Scene7 e può richiedere ulteriori licenze. Per ulteriori informazioni, contattate il supporto Scene7.

*[!DNL renderRequest]* è la normale richiesta di rendering FXG, escluso il percorso principale HTTP  ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>I caratteri di delimitazione ( `'(',')'`) e i caratteri di delimitazione dei comandi ( `'?'`, `'&'`, `'='`) all&#39;interno delle richieste nidificate non devono essere codificati per HTTP. In effetti, le richieste incorporate devono essere codificate come la richiesta esterna (incorporazione).

I seguenti comandi FXG vengono ignorati quando specificati in richieste nidificate:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Sorgenti di immagini esterne {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

Image Server supporta l’accesso alle immagini sorgente su server HTTP esterni.

>[!NOTE]
>
>Per gli URL remoti è supportato solo il protocollo HTTP.

Per specificare un URL esterno per un comando `src=` o `mask=`, delimitare l&#39;URL esterno o il frammento URL con le parentesi:

`…&src=( foreignUrl)&…`

Importante I caratteri di delimitazione ( `'(',')'`) e i caratteri di delimitazione dei comandi ( `'?'`, `'&'`, `'='`) nelle richieste nidificate non devono essere codificati per HTTP. In effetti, le richieste incorporate devono essere codificate come la richiesta esterna (incorporazione).

Sono consentiti URL assoluti completi (se è impostato `attribute::AllowDirectUrls`) e URL relativi a `attribute::RootUrl`. Si verifica un errore se un URL assoluto è incorporato e attributo: `AllowDirectUrls` è 0 oppure se è specificato un URL relativo e `attribute::RootUrl` è vuoto.

Sebbene gli URL esteri non possano essere specificati direttamente nel componente percorso dell’URL della richiesta, è possibile impostare una regola di pre-elaborazione per consentire la conversione di percorsi relativi in URL assoluti (vedere l’esempio di seguito).

Le immagini esterne vengono memorizzate nella cache dal server in base alle intestazioni di cache incluse nella risposta HTTP. Se non è presente un&#39;intestazione di risposta HTTP `ETag` o Ultima modifica, la risposta non viene memorizzata nella cache. Ciò può causare prestazioni scadenti per gli accessi ripetuti alla stessa immagine esterna, in quanto Image Server deve recuperare e convalidare nuovamente l’immagine a ogni accesso.

Questo meccanismo supporta gli stessi formati di file immagine supportati dall’utility Image Convert (IC), ad eccezione delle immagini sorgente con 16 bit per componente.

>[!NOTE]
>
>Image Serving esegue automaticamente l&#39;utility validate al primo utilizzo di un&#39;immagine esterna, per assicurarsi che l&#39;immagine sia valida e non sia danneggiata durante la trasmissione. Ciò può causare un leggero ritardo nel primo accesso. Per ottenere prestazioni ottimali, si consiglia di limitare le dimensioni di tali immagini e/o di utilizzare un formato di file immagine che consenta una buona compressione.

## Restrizioni {#section-fb68e3f0d40947feb94d7bf183b64929}

Le dimensioni dell&#39;immagine generata dalle richieste nidificate o incorporate vengono normalmente ottimizzate automaticamente. Se è abilitata la memorizzazione nella cache delle immagini delle richieste nidificate, è possibile ottenere miglioramenti in termini di prestazioni specificando la dimensione esatta dell&#39;immagine nidificata, in modo che non sia necessario eseguire ulteriori modifiche in scala quando si riutilizza la voce della cache.

Il server immagini importante non supporta la doppia codifica delle richieste nidificate o incorporate. Le richieste nidificate e incorporate devono essere codificate tramite HTTP esattamente come le semplici richieste.

## Esempi {#section-d800cfc31abe46d2a964f8e7929231f1}

**Modello con livelli con memorizzazione nella cache:**

Utilizzate la nidificazione per aggiungere il caching a un modello di livelli. Un numero limitato di immagini di sfondo viene sovrapposto a testo molto variabile. La stringa del modello iniziale potrebbe essere simile alla seguente:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Con lievi modifiche, possiamo preridimensionare l’immagine del livello 0 e memorizzarla nella cache in modo permanente, riducendo così il carico del server:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Incorporazione di richieste per il rendering delle immagini Scene7**

Utilizzo di un modello memorizzato in [!DNL myCatalog/myTemplate]; generate l’immagine per il livello2 del modello utilizzando Scene7 Image Rendering:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Notate le parentesi graffe nidificate. La richiesta di Image Rendering incorpora una chiamata a Image Server per recuperare una texture ripetibile.

## Consultate anche {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [Request PreProcessing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Image Rendering Reference,  [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [Image Serving Utilities](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
