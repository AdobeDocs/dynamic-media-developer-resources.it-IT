---
description: Dati set di immagini. Fornisce un meccanismo per definire set ordinati di immagini e controllare gli attributi utilizzati dai visualizzatori Dynamic Media.
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# ImageSet{#imageset}

Dati set di immagini. Fornisce un meccanismo per definire set ordinati di immagini e controllare gli attributi utilizzati dai visualizzatori Dynamic Media.

Un set di immagini è costituito da un elenco di elementi ordinato, separato da virgole. Ogni elemento è costituito da uno o più elementi secondari (ID immagine, ID campione, percorsi di file multimediali, etichette e così via), separati da punti e virgola, due punti o entrambi.

Le parentesi graffe `{ }` e le parentesi graffe `( )` possono essere utilizzate per delimitare alcuni contenuti (ad esempio i valori di colore) o indicare set nidificati. Le parentesi graffe utilizzate in questo modo non devono essere codificate e devono sempre essere visualizzate come coppie corrispondenti, altrimenti si verifica un errore di analisi del catalogo.

>[!NOTE]
>
>I seguenti caratteri vengono utilizzati come delimitatori set e devono essere codificati HTTP quando vengono visualizzati nel set come parte di valori ID o stringa:
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`


Per ulteriori informazioni sulla struttura e sull’utilizzo dei set di immagini, consulta la documentazione dei visualizzatori Image Server.

Il server restituisce il contenuto di questo campo senza modifiche in risposta a una richiesta `req=imageset`.

## Set standard {#section-5ecc8ffee7224668b63f601383665564}

Le seguenti definizioni di set sono supportate in modo nativo da Image Server e l&#39;accesso con alcuni visualizzatori comporta l&#39;analisi, la convalida e l&#39;elaborazione lato server del set. Ogni tipo di set può essere identificato specificando il valore corrispondente in `catalog::AssetType`.

**Set di campioni di base**

Ogni elemento di un set di campioni di base è costituito da un riferimento a un record immagine e da un riferimento separato facoltativo a un record immagine utilizzato come campione.

| `*`basicSwatchSet`*` | `*`swatchItem`*&#42;[',' *`swatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*`imageId`*[';' *`campione`*]` |
| `*`campione`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | Riferimento immagine IS (catalogo/id) |
| `*`swatchId`*` | Riferimento immagine IS (catalogo/id) |
| `*`solidColorSpecifier`*` | ` '{0x' *`rggbb`* [ *`etichetta`*]'}'` |
| `*`rggbb`*` | Valore colore RGB esadecimale a 6 cifre per campioni di colore a tinta unita |
| `*`etichetta`*` | Etichetta di testo opzionale per campioni di colore uniforme |

**Set di campioni gerarchici**

Ogni elemento di un set di campioni gerarchico può essere costituito da un elemento campione di base o da un riferimento a un record del set di campioni (per tali elementi sono necessari campioni).

| `*`hierarchicalSwatchSet`*` | `*`hierarchicalSwatchItem`* &#42;[ ',' *`hierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*`swatchItem`* | { *`basicSwatchSetId`* ';' *`swatch`* }` |
| `*`basicSwatchSetId`*` | Riferimento IS (catalogo/id) a un record di catalogo che definisce un set di campioni di base |

**Set 360 gradi di base**

Un set 360 gradi di base è costituito da un semplice elenco di ID immagine.

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**Set 360 Gradi Bidimensionali**

Ogni elemento di un set 360 gradi bidimensionale può essere costituito da un&#39;immagine semplice, da un riferimento a un set 360 gradi di base o da un set 360 gradi di base in linea delimitato da parentesi graffe. Al posto delle parentesi graffe è possibile utilizzare le parentesi graffe.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`* | { '{' *`basicSpinSet`* '}' } | *`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | Riferimento IS (catalogo/id) a un record di catalogo che definisce un set 360 gradi di base |

**Set di pagine**

Ogni elemento di un set di pagine può essere costituito da un massimo di immagini di tre pagine separate da due punti.

| `*`setPagine`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**Set di file multimediali**

Ogni elemento di un set di file multimediali può essere costituito da un’immagine, un set di campioni di base, un set di campioni gerarchico, un set 360 gradi di base, un set 360 gradi bidimensionale, un set di pagine o una risorsa video. Ogni elemento del set di file multimediali può anche contenere un campione facoltativo e un identificatore del tipo.

| `*`mediaSet`*` | `*`elemento`* &#42;[ , *`elemento`* ]` |
|---|---|
| `*`elemento`*` | ` { *`videoItem`* | *`remixItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`prenotato`* ] ] ]` |
| `*`elementoVideo`*` | `*`video`* ; *`ID campione`*` |
| `*`remixItem`*` | `*`remix`* ; *`swatchId`*` |
| `*`elementoImmagine`*` | `*`imageId`* ; [ *`swatchId`* ]` |
| `*`setItem`*` | ` { *`setId`* | { '{' *`inlineSet`* '}' } } ; *`swatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | ID immagine IS |
| `*`video`*` | Percorso file video/animazione o ID catalogo statico |
| `*`remix`*` | Percorso file XML di definizione remix o ID catalogo statico |
| `*`imageId`*` | ID immagine IS |
| `*`setId`*` | Riferimento IS a image, spin o ecatalog set |
| `*`inlineSet`*` | Immagine, rotazione o set di cataloghi allineati |
| `*`riservato`*` | Riservato per uso futuro |

**Set video**

Un set video è costituito da un semplice elenco di ID video in cui ogni ID fa riferimento a una voce nel catalogo dei contenuti statici.

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## Proprietà {#section-17c731e5c46646aa90ac21f39bb693ca}

Stringa di testo. Elenco separato da virgole di valori `catalog::Id`, percorsi assoluti dei file del server immagini o percorsi dei file relativi a `attribute::RootPath`. È possibile fare riferimento alla stessa immagine più di una volta nel set. Il record catalogo di definizione può essere visualizzato nel set in qualsiasi posizione.

Questo campo partecipa alla localizzazione delle stringhe di testo. Oltre a *`label`* stringhe (parte di *`solidColorSpecifier`*), tutti i campi delimitati sono localizzati se includono almeno un token di localizzazione &#39; `^loc=…^`&#39;. Per ulteriori informazioni, consultare [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) nella *documentazione sul protocollo HTTP*.

## Predefinito {#section-c3a60e360393478284f0f2d2da5b963b}

Nessuno.

## Vedi anche {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [Traduzione ID oggetto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) , [Localizzazione stringa di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Documentazione visualizzatori Image Server
