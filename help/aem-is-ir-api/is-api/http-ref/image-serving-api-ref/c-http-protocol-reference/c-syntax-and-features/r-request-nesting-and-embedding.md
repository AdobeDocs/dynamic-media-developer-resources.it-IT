---
description: Image Server supporta la nidificazione illimitata delle richieste Image Server, l’incorporamento delle richieste Image Rendering e l’incorporamento delle immagini recuperate da server esterni. Solo le immagini e le maschere di livello supportano questi meccanismi.
solution: Experience Manager
title: Richiedi nidificazione e incorporamento
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# Richiedi nidificazione e incorporamento{#request-nesting-and-embedding}

Image Server supporta la nidificazione illimitata delle richieste Image Server, l’incorporamento delle richieste Image Rendering e l’incorporamento delle immagini recuperate da server esterni. Solo le immagini e le maschere di livello supportano questi meccanismi.

>[!NOTE]
>
>Alcuni client e-mail e server proxy possono codificare le parentesi graffe utilizzate per la sintassi di nidificazione e incorporamento. Le applicazioni per le quali si è verificato un problema devono utilizzare le parentesi anziché le parentesi graffe.

## Richieste di Image Server nidificate {#section-6954202119e0466f8ff27c79f4f039c8}

È possibile utilizzare un&#39;intera richiesta Image Server come origine di livello specificandola nel comando `src=` (o `mask=`) utilizzando la sintassi seguente:

`…&src=is( nestedRequest)&…`

Il token `is` distingue tra maiuscole e minuscole.

La richiesta nidificata non deve includere il percorso radice del server (in genere ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>I caratteri delimitatori di richiesta nidificati ( `'(',')'`) e i caratteri delimitatori di comando ( `'?'`, `'&'`, `'='`) all&#39;interno delle richieste nidificate non devono essere codificati HTTP. Di fatto, le richieste nidificate devono essere codificate come la richiesta esterna (nidificazione).

Le regole di pre-elaborazione vengono applicate alle richieste nidificate.

I seguenti comandi vengono ignorati se specificati nelle richieste nidificate (nell&#39;URL della richiesta oppure in `catalog::Modifier` o `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Se l&#39;immagine risultante delle richieste nidificate include dati di maschera (alfa), questa viene passata al livello di incorporamento come maschera di livello.

Vengono ignorati anche `attribute::MaxPix` e `attribute::DefaultPix` del catalogo immagini applicabile alla richiesta nidificata.

Il risultato immagine di una richiesta IS nidificata può essere memorizzato nella cache facoltativamente includendo `cache=on`. Per impostazione predefinita, la memorizzazione nella cache dei dati intermedi è disabilitata. La memorizzazione in cache deve essere abilitata solo quando si prevede che l’immagine intermedia venga riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. Si applica la gestione della cache lato server standard. I dati vengono memorizzati nella cache in un formato senza perdita di dati.

## Richieste di rendering immagini incorporate {#section-69c5548db930412b9b90d9b2951a6969}

Quando Dynamic Medie Image Rendering è abilitato sul server, le richieste di rendering possono essere utilizzate come origini di livello specificandole nel comando src= (o mask=). Utilizza la seguente sintassi:

` …&src=ir( *[!DNL renderRequest]*)&…`

Il token `ir` distingue tra maiuscole e minuscole.

*[!DNL renderRequest]* è la solita richiesta di Image Rendering, escluso il percorso radice HTTP ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>I caratteri delimitatori di richiesta nidificati ( `'(',')'`) e i caratteri delimitatori di comando ( `'?'`, `'&'`, `'='`) all&#39;interno delle richieste nidificate non devono essere codificati HTTP. Di fatto, le richieste incorporate devono essere codificate come la richiesta esterna (incorporante).

I seguenti comandi di Image Rendering vengono ignorati se specificati nelle richieste nidificate:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Vengono ignorati anche `attribute::MaxPix` e `attribute::DefaultPix` del catalogo dei materiali che si applica alla richiesta di rendering nidificata.

Il risultato immagine di una richiesta a infrarossi nidificata può essere memorizzato nella cache facoltativamente includendo `cache=on`. Per impostazione predefinita, la memorizzazione nella cache dei dati intermedi è disabilitata. La memorizzazione in cache deve essere abilitata solo quando si prevede che l’immagine intermedia venga riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. Si applica la gestione della cache lato server standard. I dati vengono memorizzati nella cache in un formato senza perdita di dati.

## Richieste di rendering FXG incorporate {#section-c817e4b4f7da414ea5a51252ca7e120a}

Quando il renderer grafico FXG (o [!DNL AGMServer]) è installato e abilitato con Image Server, le richieste FXG possono essere utilizzate come origini di livello specificandole nei comandi `src=` (o `mask=`). Utilizza la seguente sintassi:

`…&src=fxg( renderRequest)&…`

Il token `fxg` distingue tra maiuscole e minuscole.

>[!NOTE]
>
>Il rendering della grafica FXG è disponibile solo nell’ambiente in hosting Dynamic Medie e potrebbe richiedere licenze aggiuntive. Per ulteriori informazioni, contattare il supporto tecnico Dynamic Medie.

*[!DNL renderRequest]* è la richiesta di rendering FXG usuale, escluso il percorso radice HTTP ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>I caratteri delimitatore ( `'(',')'`) e i caratteri delimitatore comando ( `'?'`, `'&'`, `'='`) all&#39;interno delle richieste nidificate non devono essere codificati HTTP. Di fatto, le richieste incorporate devono essere codificate come la richiesta esterna (incorporante).

I seguenti comandi FXG vengono ignorati se specificati nelle richieste nidificate:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Origini immagine esterne {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

Image Server supporta l’accesso alle immagini sorgente su server HTTP esterni.

>[!NOTE]
>
>Per gli URL remoti è supportato solo il protocollo HTTP.

Per specificare un URL esterno per un comando `src=` o `mask=`, delimitare l&#39;URL esterno o il frammento di URL con parentesi:

`…&src=( foreignUrl)&…`

Importante I caratteri delimitatore ( `'(',')'`) e i caratteri delimitatore comando ( `'?'`, `'&'`, `'='`) all&#39;interno delle richieste nidificate non devono essere codificati HTTP. Di fatto, le richieste incorporate devono essere codificate come la richiesta esterna (incorporante).

Sono consentiti URL assoluti completi (se è impostato `attribute::AllowDirectUrls`) e URL relativi a `attribute::RootUrl`. Si verifica un errore se è incorporato un URL assoluto e l&#39;attributo: `AllowDirectUrls` è 0 oppure se è specificato un URL relativo e `attribute::RootUrl` è vuoto.

Anche se gli URL esterni non possono essere specificati direttamente nel componente percorso dell’URL della richiesta, è possibile impostare una regola di preelaborazione per consentire la conversione di percorsi relativi in URL assoluti (vedi l’esempio di seguito).

Le immagini esterne vengono memorizzate nella cache dal server in base alle intestazioni di memorizzazione in cache incluse nella risposta HTTP. Se non è presente né un&#39;intestazione di risposta HTTP `ETag` né Last-Modified, la risposta non viene memorizzata in cache. Questo può causare prestazioni scadenti per gli accessi ripetuti per la stessa immagine esterna, in quanto Image Server deve recuperare e riconvalidare l’immagine a ogni accesso.

Questo meccanismo supporta gli stessi formati di file immagine supportati dall&#39;utilità di conversione delle immagini (IC), ad eccezione delle immagini sorgente con 16 bit per componente.

>[!NOTE]
>
>Image Server esegue automaticamente l&#39;utilità di convalida quando viene utilizzata per la prima volta un&#39;immagine esterna, per garantire che sia valida e non sia danneggiata durante la trasmissione. Questo può causare un leggero ritardo al primo accesso. Per ottenere prestazioni ottimali, si consiglia di limitare le dimensioni di tali immagini e/o utilizzare un formato di file di immagine che comprima bene.

## Restrizioni {#section-fb68e3f0d40947feb94d7bf183b64929}

Le dimensioni dell’immagine generata da richieste nidificate/incorporate vengono in genere ottimizzate automaticamente. Se è abilitata la memorizzazione nella cache delle immagini di richiesta nidificate, è possibile ottenere miglioramenti incrementali delle prestazioni specificando la dimensione esatta dell’immagine nidificata, in modo che non sia necessario alcun ulteriore ridimensionamento quando la voce della cache viene riutilizzata.

Il server immagini importanti non supporta la doppia codifica delle richieste nidificate o incorporate. Le richieste nidificate e incorporate devono avere la codifica HTTP proprio come per le richieste semplici.

## Esempi {#section-d800cfc31abe46d2a964f8e7929231f1}

**Modello di layout con memorizzazione nella cache:**

Utilizzare la nidificazione per aggiungere il caching a un modello di layout. Un numero limitato di immagini di sfondo viene sovrapposto a testo altamente variabile. La stringa del modello iniziale potrebbe essere simile alla seguente:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Con lievi modifiche, possiamo prescalare l&#39;immagine di livello 0 e memorizzarla nella cache in modo persistente, riducendo così il carico del server:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Richieste di incorporamento per il rendering immagini Dynamic Medie**

Utilizzando un modello archiviato in [!DNL myCatalog/myTemplate]; generare l&#39;immagine per il livello 2 del modello utilizzando il rendering immagini di Dynamic Medie:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Osserva le parentesi graffe nidificate. La richiesta Image Rendering incorpora una chiamata a Image Server per recuperare una texture ripetibile.

## Consultate anche {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [PreElaborazione richieste](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), riferimento rendering immagini, [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Utilità server immagini](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
