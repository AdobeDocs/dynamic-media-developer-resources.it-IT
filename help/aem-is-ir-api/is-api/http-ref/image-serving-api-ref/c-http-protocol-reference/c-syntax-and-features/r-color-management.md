---
title: Gestione colore Image Server
description: Image Server supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1202'
ht-degree: 2%

---

# Gestione colore Image Server{#image-serving-color-management}

Image Server supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).

## Spazi colore predefiniti {#section-8cfe60808bce49968091995e4e521dba}

Ogni catalogo di immagini (e il catalogo predefinito) può definire un set di profili ICC che costituiscono gli spazi colore predefiniti per questo catalogo: un profilo di input e un profilo di output ciascuno per i dati in scala di grigio, RGB e CMYK. Consulta
[attribute::IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[attribute::IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[attribute::IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[attribute::IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[attribute::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[attribute::IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md).

## Spazio colore di input {#section-9f08e2c1b6aa4fe4815be174972c1944}

Le immagini sorgente possono incorporare profili ICC per definire lo spazio colore di input. Se in un&#39;immagine sorgente non è incorporato alcun profilo, `attribute::IccProfileSrc*` del catalogo immagini applicabile corrispondente al tipo di pixel dell’immagine sorgente. Se questo attributo non è definito nel catalogo immagini, `attribute::IccProfile*` viene utilizzato. Se nemmeno l’attributo del catalogo è definito, l’immagine non viene gestita tramite colori e vengono applicate solo le trasformazioni naïve.

## Spazio colore di output {#section-b517bca622b64dcfa7defba6035d0716}

Lo spazio colore del risultato dell’immagine finale di una richiesta è definito con `icc=` comando. Se `icc=` non è specificato, come spazio colore di output viene utilizzato lo spazio colore di output predefinito (dal catalogo principale della richiesta) che corrisponde al tipo di pixel dell’immagine di output. Se nel catalogo principale o predefinito non è definito alcun profilo di output e il livello di base è un&#39;immagine con un profilo incorporato corrispondente al tipo di pixel di output, tale profilo viene utilizzato per lo spazio colore di output. In caso contrario, lo spazio colore di output rimane indefinito: vengono applicate solo le conversioni di colore naïve durante la conversione tra tipi di pixel e nessun profilo colore può essere incorporato nell&#39;immagine di output.

Lo spazio colore di output di una richiesta Image Server nidificata/incorporata è sempre lo stesso dello spazio colore di output della richiesta di incorporamento esterna.

## Colori tinta unita {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Valori colore specificati con `color=`, `bgcolor=`o il comando RTF `\iscolortbl` sono associate allo spazio colore di input se il valore del colore include il suffisso &#39;S&#39;, altrimenti sono associate allo spazio colore di output. Valori colore specificati con `bgc=` o i comandi RTF `\colortbl` e `\cmykcolortbl` sono sempre associate allo spazio colore di output predefinito o effettivo corrispondente.

>[!NOTE]
>
>In questo momento, `bgc=` non partecipa completamente alla gestione del colore; il suffisso &#39;S&#39; viene ignorato se specificato con `bgc=`, e la conversione naïve viene applicata quando il tipo di pixel del valore di colore specificato con `bgc=` differisce dal tipo di pixel dell&#39;immagine di output. Altrimenti, `bgc=` è associato allo spazio colore di output effettivo.

## Richieste nidificate e incorporate {#section-bdda638c31504f26a77e51ebb1ea6e3b}

Lo spazio colore di output per le richieste IS nidificate e le richieste IR incorporate viene impostato automaticamente sullo spazio colore di output della richiesta più esterna, a meno che la richiesta nidificata non specifichi uno spazio colore di output esplicito con `icc=`. Inoltre, le richieste nidificate/incorporate ereditano anche gli spazi colore di output predefiniti dal catalogo principale della richiesta più esterna, per garantire una gestione coerente dei valori di colore in tinta unita.

## Conversione spazio colore {#section-ca87b80b8e364ea59d8a92d87121b0fb}

Image Server generalmente tenta di ritardare le conversioni dei colori durante l’elaborazione. Se tutti i livelli di un&#39;immagine hanno lo stesso spazio colore del livello, la conversione nello spazio colore di output viene eseguita dopo l&#39;unione e il ridimensionamento finale. Se sono interessati più spazi colore del livello, ciascun livello viene trasformato nello spazio colore di output prima dell&#39;unione.

>[!NOTE]
>
>I comandi `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=`, e `op_saturation=` sono operazioni RGB. Queste operazioni mantengono la fedeltà dei colori solo se lo spazio colore del livello è di tipo pixel RGB. Se diverso da RGB, i dati vengono convertiti in RGB utilizzando la conversione dei colori naïve e il risultato ha una fedeltà dei colori limitata. Lo spazio colore del livello per tali livelli deve essere considerato indeterminato.

Le opzioni di conversione del colore sono fornite con `icc=` o, se `icc=` non è specificato, con `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation`, e `attribute::IccDither`.

## Incorporazione dei profili colore {#section-261ebbae5ce046589a776ca972380052}

Il profilo colore ICC dello spazio colore di output, se disponibile, può essere incorporato nell&#39;immagine di risposta specificando `iccEmbed=`.

## Gestione dei profili ICC {#section-eb210e4b44e64e2c8b80ee59216c5555}

Tutti i profili colore utilizzati dal server devono essere conformi alle specifiche ICC. I file di profilo ICC hanno in genere un [!DNL .icc] o [!DNL .icm] suffisso di file e si trovano insieme ai file di dati immagine.

Mentre i profili di output possono essere specificati per percorso/nome file nel `icc=` si consiglia di registrare tutti i file di profilo nella Mappa profilo ICC del catalogo predefinito o del catalogo immagini e di utilizzare gli identificatori di scelta rapida ( `icc::Name`) invece dei percorsi dei file.

Tutti i profili ICC a cui si fa riferimento in `catalog::IccProfile` e in `attribute::IccProfile*` deve essere registrato nella mappa del profilo ICC dell&#39;immagine o del catalogo predefinito.

## Restrizioni {#section-fb50ede40b124b89b30679da29782ab5}

Al momento sono supportati solo gli spazi di colore CMYK, RGB e in scala di grigi.

## Profili colore ICC inclusi {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

Image Server include la maggior parte dei profili ICC Adobe standard nel catalogo immagini predefinito. È possibile accedere a questi profili con i loro nomi comuni (ad esempio, come si vede in Photoshop) o con un identificatore un po’ più breve. Nella tabella seguente sono elencati tutti i profili ICC standard. Quando si fa riferimento a un profilo in `icc=` con il nome comune, gli spazi devono essere codificati come `%20`.

Ulteriori profili possono essere aggiunti ai profili standard nel catalogo predefinito o in un catalogo immagini specifico. Consulta la sezione [Riferimento mappa profilo ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) per i dettagli.

>[!NOTE]
>
>La seguente tabella si applica a *Dynamic Medie ibrido* solo (in esecuzione in `dynamicmedia` modalità di esecuzione).

| Identificatore | Nome comune | Nome file |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB` | CIE RGB | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC, 1953 | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto` | ProPhoto RGB | ProPhoto.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | Profilo spazio colore sRgb.icm |
| `WideGamutRGB` | Wide Gamut RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | FOGRA27 rivestito (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | FOGRA39 rivestita (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `CoatedGraCol` | GracoL 2006 rivestito (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europa FOGRA27 con rivestimento ISO | EuropeISOCoatedFOGRA27.icc |
| `EuroscaleCoated` | Euroscale rivestita | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale senza rivestimento v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Rivestito colore Giappone 2001 | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Giornale Japan Color 2002 | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 non patinata | JapanColor2001Uncoated.icc |
| `JapanColorWebCoated` | Rivestimento Web Japan Color 2003 | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Rivestito Web Giappone (Ad) | JapanWebCoated.icc |
| `NewsprintSNAP2007` | US Newsprint (SNAP 2007) | USNewsprintSNAP2007.icc |
| `PS4Default` | CMYK predefinito di Photoshop 4 | Photoshop4DefaultCMYK.icc |
| `PS5Default` | CMYK predefinito di Photoshop 5 | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed non rivestito v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | FOGRA29 non rivestito (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `WebCoated` | SWOP (U.S. Web Coated) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | FOGRA28 rivestito con web (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `WebCoatedGrade3` | Carta rivestita SWOP 2006 Grado 3 | WebCoatedSWOP2006Grade3.icc |
| `WebCoatedGrade5` | Carta rivestita SWOP 2006 Grado 5 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | Web statunitense non rivestito v2 | USWebUncoated.icc |

La seguente tabella si applica a *Image Server Dynamic Media Classic* e *Dynamic Medie* (in esecuzione in `dynamicmedia_scene7` modalità di esecuzione).

| Identificatore | Nome comune | Nome file |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB|CIE RGB` | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC, 1953 | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto RGB` | ProPhoto RGB | ProPhoto RGB.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | Profilo spazio colore sRgb.icm |
| `WideGamutRGB` | Wide Gamut RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | FOGRA27 rivestito (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | FOGRA39 rivestita (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `Coated GRACoL 2006 (ISO 12647-2:2004)` | GracoL 2006 rivestito (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europa FOGRA27 con rivestimento ISO | EuropeISOCoatedFOGRA27.icc |
| `Euroscale Coated v2` | Euroscale rivestita v2 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale senza rivestimento v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Rivestito colore Giappone 2001 | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Giornale Japan Color 2002 | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 non patinata | JapanColor2001Uncoated.icc |
| `Japan Color 2003 Web Coated` | Rivestimento Web Japan Color 2003 | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Rivestito Web Giappone (Ad) | JapanWebCoated.icc |
| `PS4Default` | CMYK predefinito di Photoshop 4 | Photoshop4DefaultCMYK.icc |
| `PS5Default` | CMYK predefinito di Photoshop 5 | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed non rivestito v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | FOGRA29 non rivestito (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `US Newsprint (SNAP 2007)` | US Newsprint (SNAP 2007) | USNewsprintSNAP2007.icc |
| `WebCoated` | SWOP (U.S. Web Coated) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | FOGRA28 rivestito con web (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `Web Coated SWOP 2006 Grade 3 Paper` | Carta rivestita SWOP 2006 Grado 3 | WebCoatedSWOP2006Grade3.icc |
| `Web Coated SWOP Grade 5 Paper` | Carta rivestita SWOP 2006 Grado 5 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | Web statunitense non rivestito v2 | USWebUncoated.icc |

## Consultate anche {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;, [attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;, [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::Compensazione punto nero Icc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [Riferimento mappa profilo ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color= colore](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
