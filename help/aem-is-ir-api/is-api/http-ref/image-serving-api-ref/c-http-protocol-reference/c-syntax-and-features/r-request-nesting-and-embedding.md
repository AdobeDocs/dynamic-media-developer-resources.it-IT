---
description: Image Serving supporta la nidificazione illimitata delle richieste di Image Server, l’incorporazione di richieste di Image Rendering e l’incorporazione di immagini recuperate da server stranieri. Solo le immagini di livello e le maschere di livello supportano questi meccanismi.
solution: Experience Manager
title: Nidificazione e incorporazione delle richieste
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Nidificazione e incorporazione delle richieste{#request-nesting-and-embedding}

Image Serving supporta la nidificazione illimitata delle richieste di Image Server, l’incorporazione di richieste di Image Rendering e l’incorporazione di immagini recuperate da server stranieri. Solo le immagini di livello e le maschere di livello supportano questi meccanismi.

>[!NOTE]
>
>Alcuni client e-mail e server proxy possono codificare le parentesi graffe utilizzate per la sintassi di nidificazione e incorporamento. Le applicazioni per le quali si tratta di un problema devono utilizzare parentesi al posto delle parentesi graffe.

## Richieste Image Server nidificate {#section-6954202119e0466f8ff27c79f4f039c8}

Un&#39;intera richiesta di Image Server può essere utilizzata come origine di livello specificandola nel comando `src=` (o `mask=`) utilizzando la seguente sintassi:

`…&src=is( nestedRequest)&…`

Il token `is` fa distinzione tra maiuscole e minuscole.

La richiesta nidificata non deve includere il percorso principale del server (in genere ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>I caratteri di delimitazione della richiesta nidificati ( `'(',')'`) e i caratteri di delimitazione dei comandi ( `'?'`, `'&'`, `'='`) nelle richieste nidificate non devono essere codificati tramite HTTP. Di fatto, le richieste nidificate devono essere codificate come la richiesta esterna (nidificazione).

Le regole di preelaborazione vengono applicate alle richieste nidificate.

I seguenti comandi vengono ignorati quando specificati nelle richieste nidificate (nell’URL della richiesta o in `catalog::Modifier` o `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Se l&#39;immagine del risultato delle richieste nidificate include dati di maschera (alfa), viene passata al livello di incorporamento come maschera di livello.

Vengono inoltre ignorati `attribute::MaxPix`e `attribute::DefaultPix` del catalogo immagini applicato alla richiesta nidificata.

Il risultato immagine di una richiesta IS nidificata può essere memorizzato nella cache facoltativamente includendo `cache=on`. Per impostazione predefinita, la memorizzazione in cache dei dati intermedi è disabilitata. La memorizzazione in cache deve essere abilitata solo quando ci si aspetta che l&#39;immagine intermedia venga riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. Si applica la gestione standard della cache lato server. I dati vengono memorizzati nella cache in un formato senza perdita di dati.

## Richieste di rendering immagini incorporate {#section-69c5548db930412b9b90d9b2951a6969}

Quando Dynamic Media Image Rendering è abilitato sul server, le richieste di rendering possono essere utilizzate come sorgenti di livello specificandole nel comando src= (o mask=). Utilizza la sintassi seguente:

` …&src=ir( *[!DNL renderRequest]*)&…`

Il token `ir` fa distinzione tra maiuscole e minuscole.

*[!DNL renderRequest]* è la consueta richiesta di Image Rendering, escluso il percorso principale HTTP  ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>I caratteri di delimitazione della richiesta nidificati ( `'(',')'`) e i caratteri di delimitazione dei comandi ( `'?'`, `'&'`, `'='`) nelle richieste nidificate non devono essere codificati tramite HTTP. Di fatto, le richieste incorporate devono essere codificate come la richiesta esterna (incorporazione).

I seguenti comandi Image Rendering vengono ignorati quando specificati nelle richieste nidificate:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Vengono inoltre ignorati `attribute::MaxPix` e `attribute::DefaultPix` del catalogo dei materiali applicabile alla richiesta di rendering nidificata.

Il risultato immagine di una richiesta IR nidificata può essere memorizzato nella cache facoltativamente includendo `cache=on`. Per impostazione predefinita, la memorizzazione in cache dei dati intermedi è disabilitata. La memorizzazione in cache deve essere abilitata solo quando ci si aspetta che l&#39;immagine intermedia venga riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. Si applica la gestione standard della cache lato server. I dati vengono memorizzati nella cache in un formato senza perdita di dati.

## Richieste di rendering FXG incorporate {#section-c817e4b4f7da414ea5a51252ca7e120a}

Quando il renderer grafico FXG (aka [!DNL AGMServer]) è installato e abilitato con Image Serving, le richieste FXG possono essere utilizzate come sorgenti di livello specificandole nei comandi `src=` (o `mask=`). Utilizza la sintassi seguente:

`…&src=fxg( renderRequest)&…`

Il token `fxg` fa distinzione tra maiuscole e minuscole.

>[!NOTE]
>
>Il rendering grafico FXG è disponibile solo nell’ambiente ospitato da Dynamic Media e può richiedere licenze aggiuntive. Per ulteriori informazioni, contatta il supporto tecnico Dynamic Media.

*[!DNL renderRequest]* è la normale richiesta di rendering FXG, escludendo il percorso principale HTTP  ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>I caratteri di delimitazione ( `'(',')'`) e i caratteri di delimitazione dei comandi ( `'?'`, `'&'`, `'='`) nelle richieste nidificate non devono essere codificati tramite HTTP. Di fatto, le richieste incorporate devono essere codificate come la richiesta esterna (incorporazione).

I seguenti comandi FXG vengono ignorati quando specificati nelle richieste nidificate:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Origini immagine straniere {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

Image Server supporta l&#39;accesso alle immagini sorgente su server HTTP esterni.

>[!NOTE]
>
>Per gli URL remoti è supportato solo il protocollo HTTP.

Per specificare un URL esterno per un comando `src=` o `mask=` , delimita l’URL esterno o il frammento dell’URL con parentesi:

`…&src=( foreignUrl)&…`

Importante I caratteri di delimitazione ( `'(',')'`) e i caratteri di delimitazione dei comandi ( `'?'`, `'&'`, `'='`) nelle richieste nidificate non devono essere codificati in HTTP. Di fatto, le richieste incorporate devono essere codificate come la richiesta esterna (incorporazione).

Sono consentiti gli URL completi assoluti (se è impostato `attribute::AllowDirectUrls`) e gli URL relativi a `attribute::RootUrl` . Si verifica un errore se un URL assoluto è incorporato e attributo: `AllowDirectUrls` è 0 oppure se è specificato un URL relativo e `attribute::RootUrl` è vuoto.

Sebbene gli URL stranieri non possano essere specificati direttamente nel componente percorso dell’URL di richiesta, è possibile impostare una regola di preelaborazione per consentire la conversione di percorsi relativi a URL assoluti (vedi l’esempio seguente).

Le immagini esterne vengono memorizzate nella cache dal server in base alle intestazioni di memorizzazione nella cache incluse nella risposta HTTP. Se non è presente né un&#39;intestazione di risposta HTTP `ETag` né un&#39;intestazione di risposta HTTP Last-Modified, la risposta non viene memorizzata nella cache. Questo può causare prestazioni scadenti per gli accessi ripetuti per la stessa immagine esterna, in quanto Image Serving deve recuperare e riconvalidare l&#39;immagine a ogni accesso.

Questo meccanismo supporta gli stessi formati di file immagine supportati dall&#39;utility Image Convert (IC), ad eccezione delle immagini sorgente con 16 bit per componente.

>[!NOTE]
>
>Image Serving eseguirà automaticamente l&#39;utilità validate quando viene utilizzata per la prima volta un&#39;immagine esterna, per assicurarsi che l&#39;immagine sia valida e non sia stata danneggiata durante la trasmissione. Ciò può causare un leggero ritardo nel primo accesso. Per ottenere le migliori prestazioni, si consiglia di limitare le dimensioni di tali immagini e/o di utilizzare un formato di file immagine che comprime bene.

## Restrizioni {#section-fb68e3f0d40947feb94d7bf183b64929}

Le dimensioni dell’immagine generata dalle richieste nidificate/incorporate vengono normalmente ottimizzate automaticamente. Se è abilitato il caching delle immagini di richiesta nidificate, è possibile ottenere incrementi di prestazioni incrementali specificando la dimensione esatta dell’immagine nidificata, in modo che non sia necessario alcun ulteriore ridimensionamento quando viene riutilizzata la voce di cache.

Il server di immagini importante non supporta la doppia codifica delle richieste nidificate o incorporate. Le richieste nidificate e incorporate devono essere codificate tramite HTTP come le semplici richieste.

## Esempi {#section-d800cfc31abe46d2a964f8e7929231f1}

**Modello a livelli con memorizzazione in cache:**

Utilizzare la nidificazione per aggiungere la memorizzazione in cache a un modello di livelli. Un numero limitato di immagini di sfondo viene sovrapposto a testo altamente variabile. La stringa del modello iniziale potrebbe essere simile alla seguente:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Con lievi modifiche, possiamo pre-scalare l&#39;immagine del livello 0 e memorizzarla in cache in modo persistente, riducendo così il carico del server:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Incorporazione di richieste per il rendering delle immagini di Dynamic Media**

Utilizzo di un modello memorizzato in [!DNL myCatalog/myTemplate]; genera l’immagine per il livello2 del modello utilizzando Dynamic Media Image Rendering:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Notare le parentesi graffe nidificate. La richiesta Image Rendering incorpora una chiamata a Image Serving per recuperare una texture ripetibile.

## Consultate anche {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [Richiedi preProcessing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Riferimento per il rendering delle immagini,  [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), Utilità di  [Image Serving](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
