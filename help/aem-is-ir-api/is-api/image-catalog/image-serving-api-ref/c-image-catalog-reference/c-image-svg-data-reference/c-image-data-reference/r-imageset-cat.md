---
description: Dati del set di immagini. Fornisce un meccanismo per definire set ordinati di immagini e gli attributi di controllo utilizzati dai visualizzatori Dynamic Media.
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic, SDK/API, Set di immagini
role: Developer,Business Practitioner
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 2%

---

# ImageSet{#imageset}

Dati del set di immagini. Fornisce un meccanismo per definire set ordinati di immagini e gli attributi di controllo utilizzati dai visualizzatori Dynamic Media.

Un set di immagini è costituito da un elenco ordinato e separato da virgole di elementi, con ogni elemento composto da uno o più elementi secondari (ID immagine, ID campione, percorsi dei file multimediali, etichette, ecc.), separati da punti e virgola e/o due punti.

Le parentesi graffe `{ }` e `( )` possono essere utilizzate per delimitare determinati contenuti (ad esempio i valori di colore) o per indicare set nidificati. Le parentesi o parentesi utilizzate in questo modo non devono essere codificate e devono sempre apparire come coppie corrispondenti, altrimenti si verifica un errore di analisi del catalogo.

>[!NOTE]
>
>I seguenti caratteri vengono utilizzati come delimitatori impostati e devono essere codificati in HTTP quando compaiono nel set come parte dei valori id o stringa:
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



Per ulteriori informazioni sulla struttura e sull’utilizzo dei set di immagini, consulta la documentazione Image Serving Viewers .

Il server restituisce il contenuto di questo campo senza modifiche in risposta a una richiesta `req=imageset`.

## Set standard {#section-5ecc8ffee7224668b63f601383665564}

Le seguenti definizioni di set sono supportate in modo nativo da Image Serving e l&#39;accesso con alcuni visualizzatori prevede l&#39;analisi, la convalida e l&#39;elaborazione lato server del set. Ogni tipo di set può essere identificato specificando il valore corrispondente in `catalog::AssetType`.

**Set di campioni di base**

Ogni elemento di un set di campioni di base è costituito da un riferimento a un record di immagine e da un riferimento separato facoltativo a un record di immagine utilizzato come campione.

| `*`basicSwatchSet`*` | `*``*&#42;[',' *`swatchItemSwatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*``*[';' *`imageIdswatch`*]` |
| `*`campione`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | Riferimento immagine IS (catalog/id) |
| `*`swatchId`*` | Riferimento immagine IS (catalog/id) |
| `*`solidColorSpecifier`*` | ` '{0x' *``* [ *`rgbblable`*]'}'` |
| `*`rggbb`*` | Valore di colore RGB esadecimale a 6 cifre per i campioni di colore a tinta unita |
| `*`label`*` | Etichetta di testo opzionale per i campioni a colori pieni |

**Set di campioni gerarchici**

Ogni elemento in un set di campioni gerarchico può essere costituito da un elemento campione di base o da un riferimento a un record set di campioni (per tali elementi sono necessari campioni).

| `*`hierarchySwatchSet`*` | `*``* &#42;[ ',' *`hierarchySwatchItemHierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchySwatchItem`*` | `*``* | { *``* ';' *`swatchItembasicSwatchSetIdswatch`* }` |
| `*`basicSwatchSetId`*` | Riferimento IS (catalogo/id) a un record di catalogo che definisce un set di campioni di base |

**Set 360 gradi di base**

Un set 360 gradi di base è costituito da un semplice elenco di ID immagine.

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**Set 360 gradi a due dimensioni**

Ogni elemento di un set 360 gradi bidimensionale può essere costituito da un’immagine semplice, un riferimento a un set 360 gradi di base o un set 360 gradi di base in linea delimitato da parentesi graffe. Le parentesi possono essere utilizzate al posto delle parentesi graffe.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*``* | { '{' *``* '}' } | *`imageIdbasicSpinSetSpinSetId`*` |
| `*`basicSpinSetId`*` | Riferimento IS (catalogo/id) a un record di catalogo che definisce un set 360 gradi di base |

**Set di pagine**

Ogni elemento di un set di pagine può essere costituito da un massimo di tre immagini di pagina separate da due punti.

| `*`pageSet`*` | `*``* &#42;[ , *`pageItemItem`* ]` |
|---|---|
| `*`pageItem`*` | `*``* [ : *``* [ : *`imageIdimageIdimageId`* ] ]` |

**Set di file multimediali**

Ogni elemento di un set di file multimediali può essere costituito da un’immagine, un set di campioni di base, un set di campioni gerarchico, un set 360 gradi di base, un set 360 gradi bidimensionale, un set di pagine o una risorsa video. Ogni elemento del set di file multimediali può anche contenere un campione e un identificatore di tipo facoltativi.

| `*`mediaSet`*` | `*``* &#42;[ , *`elemento`* ]` |
|---|---|
| `*`item`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemRipristinaItemItemsetItemIDreserve`* ] ] ]` |
| `*`videoItem`*` | `*``* ; *`videoswatchId`*` |
| `*`RecuperaElemento`*` | `*``* ; *`recutswatchId`*` |
| `*`imageItem`*` | `*``* ; [ *`imageIdentityId`* ]` |
| `*`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | ID immagine IS |
| `*`video`*` | Percorso file video/animazione o id catalogo statico |
| `*`ricuperare`*` | Percorso del file XML di definizione del file o ID del catalogo statico |
| `*`imageId`*` | ID immagine IS |
| `*`setId`*` | Riferimento IS a un set di immagini, spin o ecatalog |
| `*`inlineSet`*` | Set di immagini, spin o ecatalog in linea |
| `*`riservato`*` | Riservato per uso futuro |

**Set video**

Un set video è costituito da un semplice elenco di id video in cui ogni id fa riferimento a una voce nel catalogo dei contenuti statici.

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## Proprietà {#section-17c731e5c46646aa90ac21f39bb693ca}

Stringa di testo. Elenco separato da virgole di valori `catalog::Id`, percorsi di file Image Server assoluti o percorsi di file relativi a `attribute::RootPath`. È possibile fare riferimento alla stessa immagine più di una volta nel set. Il record del catalogo di definizione può essere visualizzato nel set in qualsiasi posizione.

Questo campo partecipa alla localizzazione delle stringhe di testo. Oltre alle stringhe *`label`* (parte di *`solidColorSpecifier`*), tutti i campi delimitati vengono localizzati se includono almeno un token di localizzazione &#39; `^loc=…^`&#39;. Per ulteriori informazioni, consulta [Localizzazione delle stringhe di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in *Riferimento al protocollo HTTP* .

## Predefinito {#section-c3a60e360393478284f0f2d2da5b963b}

Nessuno.

## Vedi anche {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [attributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), traduzione [ ID ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) oggetto, localizzazione [ stringa di ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) testo, documentazione dei visualizzatori Image Server
