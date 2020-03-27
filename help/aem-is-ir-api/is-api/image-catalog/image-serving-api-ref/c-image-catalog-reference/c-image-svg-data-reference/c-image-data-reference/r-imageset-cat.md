---
description: Dati del set di immagini. Offre un meccanismo per definire set di immagini ordinati e gli attributi di controllo utilizzati dai visualizzatori di Scene7.
seo-description: Dati del set di immagini. Offre un meccanismo per definire set di immagini ordinati e gli attributi di controllo utilizzati dai visualizzatori di Scene7.
seo-title: ImageSet
solution: Experience Manager
title: ImageSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a34aaef-4053-4474-abb8-794331898d88
translation-type: tm+mt
source-git-commit: 06f227705765e4173e1c4b49dd7d8202884f5e07

---


# Set di immagini{#imageset}

Dati del set di immagini. Offre un meccanismo per definire set di immagini ordinati e gli attributi di controllo utilizzati dai visualizzatori di Scene7.

Un set di immagini è composto da un elenco di elementi ordinati e separati da virgole, ciascuno dei quali è composto da uno o più elementi secondari (ID immagine, ID campioni, percorsi di file multimediali, etichette ecc.), separati da punti e virgola e/o due punti.

Le parentesi graffe &#39;{ }&#39; e &#39;( )&#39; possono essere utilizzate per delimitare alcuni contenuti (come i valori di colore) o per indicare set nidificati. Le parentesi o le parentesi utilizzate in questo modo non devono essere codificate e devono sempre essere visualizzate come coppie corrispondenti, altrimenti si verificherà un errore di analisi del catalogo.

>[!NOTE]
>
>I seguenti caratteri vengono utilizzati come delimitatori di set e devono essere codificati per HTTP quando compaiono nel set come parte di valori id o stringa:
>
>* ,
>* ;
>* :
>* {
>* }
>* (
>* )



Per ulteriori informazioni sulla struttura e l’utilizzo dei set di immagini, consultate la documentazione dei visualizzatori Image Server.

Il server restituisce il contenuto di questo campo senza modifiche in risposta a una `req=imageset` richiesta.

## Set standard {#section-5ecc8ffee7224668b63f601383665564}

Le seguenti definizioni di set sono supportate in modo nativo da Image Server e l’accesso con alcuni visualizzatori richiede l’analisi, la convalida e l’elaborazione lato server del set. Ogni tipo di set può essere identificato specificando il valore corrispondente in `catalog::AssetType`.

**Set di campioni di base**

Ogni elemento in un set di campioni di base è costituito da un riferimento a un record di immagine e da un riferimento separato facoltativo a un record di immagine utilizzato come campione.

| ` *`basicSwatchSet`*` | ` *``*&#42;[',' *`swatchItemSwatchItem`*]` |
|---|---|
| ` *`swatchItem`*` | ` *``*[';' *`imageIdswatch`*]` |
| ` *`campione`*` | ` *`swatchId`*|solidColorSpecifier` |
| ` *`imageId`*` | Riferimento immagine IS (catalog/id) |
| ` *`swatchId`*` | Riferimento immagine IS (catalog/id) |
| ` *`solidColorSpecifier`*` | ` '{0x' *``* [ *`rgbblabel`*]'}'` |
| ` *`rggbb`*` | Valore del colore RGB esadecimale a 6 cifre per i campioni in tinta unita |
| ` *`label`*` | Etichetta di testo opzionale per i campioni in tinta unita |

**Set di campioni gerarchici**

Ogni elemento di un set di campioni gerarchico può essere costituito da un elemento campione di base o da un riferimento a un record di set di campioni (per tali elementi sono necessari dei campioni).

| ` *`hierarchySwatchSet`*` | ` *``* &#42;[ ',' *`gerarchicoSwatchItemgerarchicoSwatchItem`* ]` |
|---|---|
| ` *`hierarchySwatchItem`*` | ` *``* | { *``* ';' *`swatchItembasicSwatchSetIdswatch`* }` |
| ` *`basicSwatchSetId`*` | Riferimento IS (catalogo/id) a un record di catalogo che definisce un set di campioni di base |

**Set 360 gradi di base**

Un set 360 gradi di base è costituito da un semplice elenco di ID immagine.

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**Set 360 gradi bidimensionali**

Ogni elemento in un set 360 gradi bidimensionale può essere costituito da un’immagine semplice, un riferimento a un set 360 gradi di base o un set 360 gradi di base in linea delimitato da parentesi graffe. È possibile utilizzare le parentesi al posto delle parentesi graffe.

| ` *`2dSpinItem`*` | ` *`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| ` *`2dSpinItem`*` | ` *``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| ` *`basicSpinSetId`*` | Riferimento IS (catalogo/id) a un record di catalogo che definisce un set 360 gradi di base |

**Set di pagine**

Ogni elemento in un set di pagine può essere costituito da un massimo di tre immagini di pagina separate da due punti.

| ` *`pageSet`*` | ` *``* &#42;[ , *`pageItemItem`* ]` |
|---|---|
| ` *`pageItem`*` | ` *``* [ : *``* [ : *`imageIdimageIdimageId`* ] ]` |

**Set di file multimediali**

Ogni elemento di un set di file multimediali può essere costituito da un’immagine, un set di campioni di base, un set di campioni gerarchico, un set 360 gradi di base, un set 360 gradi bidimensionale, un set di pagine o una risorsa video. Ogni elemento del set di file multimediali può contenere anche un identificatore di campioni e di tipi opzionale.

| ` *`mediaSet`*` | ` *``* &#42;[ , *`item`* ]` |
|---|---|
| ` *`item`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemRemixItemsetItemIDReserved`* ] ] ]` |
| ` *`videoItem`*` | ` *``* ; *`videoswatchId`*` |
| ` *`remixItem`*` | ` *``* ; *`recutswatchId`*` |
| ` *`imageItem`*` | ` *``* ; [ *`imageIdswatchId`* ]` |
| ` *`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| ` *`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| ` *`swatchId`*` | ID immagine IS |
| ` *`video`*` | Percorso del file video/animazione o ID del catalogo statico |
| ` *`remix`*` | Percorso del file XML della definizione del remix o ID del catalogo statico |
| ` *`imageId`*` | ID immagine IS |
| ` *`setId`*` | Riferimento IS a immagine, set 360 gradi o set di cataloghi |
| ` *`inlineSet`*` | Set di immagini, set 360 gradi o eCatalog in linea |
| ` *`riservato`*` | Riservato per uso futuro |

**Set video**

Un set video consiste in un semplice elenco di ID video in cui ogni ID fa riferimento a una voce nel catalogo dei contenuti statici.

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## Proprietà {#section-17c731e5c46646aa90ac21f39bb693ca}

Stringa di testo. Elenco di `catalog::Id` valori separati da virgole, percorso assoluto del file del server immagini o percorsi di file relativi a `attribute::RootPath`. È possibile fare riferimento più volte alla stessa immagine nel set. Il record del catalogo di definizione può essere visualizzato nel set in qualsiasi posizione.

Questo campo partecipa alla localizzazione delle stringhe di testo. Oltre alle *`label`* stringhe (parte di *`solidColorSpecifier`*), tutti i campi delimitati sono localizzati se includono almeno un token di localizzazione &#39; `^loc=…^`&#39;. Per ulteriori informazioni, vedere Localizzazione [delle stringhe di](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) testo nella Guida di riferimento *del protocollo* HTTP.

## Predefinito {#section-c3a60e360393478284f0f2d2da5b963b}

Nessuno.

## See Also {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), Traduzione [ID](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) oggetto, Localizzazione [stringa di](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) testo, Documentazione visualizzatori Image Server
