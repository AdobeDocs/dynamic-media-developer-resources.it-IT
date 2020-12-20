---
description: Image Serving supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).
seo-description: Image Serving supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).
seo-title: Gestione del colore Image Server
solution: Experience Manager
title: Gestione del colore Image Server
topic: Scene7 Image Serving - Image Rendering API
uuid: 6291372e-ec4c-4fbd-bffc-b55b1bf2f8cf
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '1219'
ht-degree: 0%

---


# Gestione del colore Image Server{#image-serving-color-management}

Image Serving supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).

## Spazi colore predefiniti {#section-8cfe60808bce49968091995e4e521dba}

Ogni catalogo di immagini (e il catalogo predefinito) può definire un set di profili ICC che costituiscono gli spazi colore predefiniti per questo catalogo: un input e un profilo di output ciascuno per i dati in scala di grigio, RGB e CMYK. Vedere ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`, ` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`, ` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`, ` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`, ` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)` e ` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`.

## Spazio colore di ingresso {#section-9f08e2c1b6aa4fe4815be174972c1944}

Le immagini sorgente possono incorporare profili ICC per definire lo spazio colore di input. Se non viene incorporato alcun profilo in un&#39;immagine sorgente, verrà utilizzato `attribute::IccProfileSrc*` del catalogo immagini applicabile corrispondente al tipo di pixel dell&#39;immagine sorgente. Se questo attributo non è definito nel catalogo immagini, viene utilizzato `attribute::IccProfile*`. Se l’attributo del catalogo non è definito, l’immagine non è gestita per il colore e verranno applicate solo trasformazioni ingenue.

## Spazio colore di output {#section-b517bca622b64dcfa7defba6035d0716}

Lo spazio colore del risultato finale dell&#39;immagine di una richiesta è definito con il comando `icc=`. Se `icc=` non è specificato, come spazio colore di output viene utilizzato lo spazio colore di output predefinito (dal catalogo principale della richiesta) che corrisponde al tipo di pixel dell&#39;immagine di output. Se nel catalogo principale o predefinito non è definito alcun profilo di output e se il livello di base è un’immagine con un profilo incorporato che corrisponde al tipo di pixel di output, tale profilo viene utilizzato per lo spazio colore di output. In caso contrario, lo spazio colore di output rimane indefinito: durante la conversione tra i tipi di pixel verranno applicate solo conversioni di colore ingenue; nell’immagine di output non sarà possibile incorporare alcun profilo colore.

Lo spazio colore di output di una richiesta Image Server nidificata/incorporata è sempre lo stesso dello spazio colore di output della richiesta di incorporamento esterna.

## Colori solidi {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

I valori di colore specificati con `color=`, `bgcolor=` o il comando RTF `\iscolortbl` saranno associati allo spazio colore di input se il valore del colore include il suffisso &#39;S&#39;, altrimenti saranno associati allo spazio colore di output. I valori di colore specificati con `bgc=` o i comandi RTF `\colortbl` e `\cmykcolortbl` sono sempre associati allo spazio colore di output predefinito o effettivo corrispondente.

>[!NOTE]
>
>Al momento, `bgc=` non partecipa completamente alla gestione del colore. Il suffisso &#39;S&#39; viene ignorato se specificato con `bgc=` e viene applicata una conversione ingenua quando il tipo di pixel del valore del colore specificato con `bgc=` è diverso dal tipo di pixel dell&#39;immagine di output. In caso contrario, `bgc=` è associato allo spazio colore di output effettivo.

## Richieste nidificate e incorporate {#section-bdda638c31504f26a77e51ebb1ea6e3b}

Lo spazio colore di output per le richieste IS nidificate e le richieste IR incorporate viene impostato automaticamente sullo spazio colore di output della richiesta più esterna, a meno che la richiesta nidificata non specifichi uno spazio colore di output esplicito con `icc=`. Inoltre, le richieste nidificate/incorporate ereditano gli spazi colore di output predefiniti anche dal catalogo principale della richiesta più esterna, per garantire una gestione coerente dei valori dei colori pieni.

## Conversione dello spazio colore {#section-ca87b80b8e364ea59d8a92d87121b0fb}

Image Serving in genere tenta di ritardare le conversioni dei colori durante l’elaborazione. Se tutti i livelli di un’immagine hanno lo stesso spazio colore del livello, la conversione nello spazio colore di output viene effettuata dopo l’unione e il ridimensionamento finale. Se sono coinvolti più spazi colore del livello, ciascun livello viene trasformato nello spazio colore di output prima dell’unione.

>[!NOTE]
>
>I comandi `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=` e `op_saturation=` sono operazioni RGB. Queste operazioni mantengono la fedeltà dei colori solo se lo spazio colore del livello ha un tipo di pixel RGB. Se non è RGB, i dati vengono convertiti in RGB con una conversione dei colori ingenua e il risultato sarà una fedeltà dei colori limitata. Lo spazio colore del livello per tali livelli deve essere considerato indeterminato.

Le opzioni di conversione del colore sono fornite con `icc=` o, se `icc=` non è specificato, con `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation` e `attribute::IccDither`.

## Incorporazione di profili colore {#section-261ebbae5ce046589a776ca972380052}

Il profilo colore ICC dello spazio colore di output, se disponibile, può essere incorporato nell&#39;immagine di risposta specificando `iccEmbed=`.

## Gestione dei profili ICC {#section-eb210e4b44e64e2c8b80ee59216c5555}

Tutti i profili colore utilizzati dal server devono essere conformi alle specifiche ICC. I file di profilo ICC hanno in genere un suffisso di file [!DNL .icc] o [!DNL .icm] e si trovano in una co-posizione con i file di dati immagine.

Sebbene i profili di output possano essere specificati per percorso/nome di file nel comando `icc=`, si consiglia di registrare tutti i file di profilo nella mappa profilo ICC del catalogo o del catalogo immagini predefinito e di utilizzare identificatori di scelta rapida ( `icc::Name`) invece dei percorsi di file.

Tutti i profili ICC a cui si fa riferimento in `catalog::IccProfile` e in `attribute::IccProfile*` devono essere registrati nella mappa profilo ICC dell&#39;immagine o del catalogo predefinito.

## Restrizioni {#section-fb50ede40b124b89b30679da29782ab5}

Al momento sono supportati solo gli spazi colore CMYK, RGB e scala di grigi.

## Profili colore ICC inclusi {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

Image Server include la maggior parte dei profili ICC standard  Adobe nel catalogo immagini predefinito. Tali profili possono essere utilizzati sia con nomi comuni (ad es. in Photoshop) sia con un identificatore leggermente più breve. Nella tabella seguente sono elencati tutti i profili ICC standard. Quando si fa riferimento a un profilo nel comando `icc=` in base al nome comune, gli spazi devono essere codificati come `%20`.

È possibile aggiungere altri profili ai profili standard, al catalogo predefinito o a un catalogo di immagini specifico. Per ulteriori informazioni, fare riferimento alla [Guida di riferimento della mappa del profilo ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c).

>[!NOTE]
>
>La seguente tabella si applica solo a *Dynamic Media Hybrid* (in esecuzione in `dynamicmedia` modalità di esecuzione).

|Identificatore|Nome comune|Nome file|
| | | |
|**RGB**||
|`AdobeRGB`| Adobe RGB (1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB`|CIE RGB|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC (1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto`|ProPhoto RGB|ProPhoto.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profile.icm|
|`WideGamutRGB`|Wide Gamut RGB|Wide GamutRGB.icc|
|**CMYK**||
|`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`CoatedGraCol`|GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale non patinata v2|EuroscaleUnprotected.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc|
|`JapanColorUncoated`|Japan Color 2001 Non patinato|JapanColor2001Unprotected.icc|
|`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc|
|`NewsprintSNAP2007`|Giornale USA (SNAP 2007)|USNewsprintSNAP2007.icc|
|`PS4Default`|CMYK predefinito Photoshop 4|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5 CMYK predefinito|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|Stati Uniti Foglietto Coated v2|USSheeteatCoated.icc|
|`SheetfedUncoated`|Stati Uniti Foglietto non patinato v2|USSheetpedUnspalmato.icc|
|`UncoatedFogra29`|FOGRA29 non patinata (ISO 12647-2:2004)|Non patinataFOGRA29.icc|
|`WebCoated`|Stati Uniti Web Coated (SWOP) v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`WebCoatedGrade3`|Carta SWOP 2006 con rivestimento Web di livello 3|WebCoatedSWOP2006Grade3.icc|
|`WebCoatedGrade5`|Carta SWOP 2006 con rivestimento Web di livello 5|WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|U.S. Web non patinata v2|USWebUnspalmato.icc|

La seguente tabella si applica a *Dynamic Media Classic (Scene7) Image Serving* e *Dynamic Media* (in esecuzione in `dynamicmedia_scene7` modalità di esecuzione).

|Identificatore|Nome comune|Nome file|
| | | |
|**RGB**||
|`AdobeRGB`| Adobe RGB (1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB|CIE RGB`|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC (1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profile.icm|
|`WideGamutRGB`|Wide Gamut RGB|Wide GamutRGB.icc|
|**CMYK**||
|`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`Coated GRACoL 2006 (ISO 12647-2:2004)`|GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale non patinata v2|EuroscaleUnprotected.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc|
|`JapanColorUncoated`|Japan Color 2001 Unspalmato|JapanColor2001Non patinato.icc|
|`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc|
|`PS4Default`|CMYK predefinito Photoshop 4|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5 CMYK predefinito|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|Stati Uniti Foglietto Coated v2|USSheeteatCoated.icc|
|`SheetfedUncoated`|Stati Uniti Foglietto non patinato v2|USSheetpedUnspalmato.icc|
|`UncoatedFogra29`|FOGRA29 non patinata (ISO 12647-2:2004)|Non patinataFOGRA29.icc|
|`US Newsprint (SNAP 2007)`|Giornale USA (SNAP 2007)|USNewsprintSNAP2007.icc|
|`WebCoated`|U.S. Web Coated (SWOP) v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`Web Coated SWOP 2006 Grade 3 Paper`|Carta SWOP 2006 con rivestimento Web di livello 3|WebCoatedSWOP2006Grade3.icc|
|`Web Coated SWOP Grade 5 Paper`|Carta SWOP 2006 con rivestimento Web di livello 5|WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|Stati Uniti Web non patinata v2|USWebUnspalmato.icc|

## Consultate anche {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](http://www.color.org/index.xalter),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attributo::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*,  [attributo::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)*,  [attributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attributo::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attributo::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b),  [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c),  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
