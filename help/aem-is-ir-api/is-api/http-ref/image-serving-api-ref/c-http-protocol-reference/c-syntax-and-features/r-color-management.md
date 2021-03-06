---
title: Gestione del colore Image Serving
description: Image Serving supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '1202'
ht-degree: 0%

---

# Gestione del colore Image Serving{#image-serving-color-management}

Image Serving supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).

## Spazi colore predefiniti {#section-8cfe60808bce49968091995e4e521dba}

Ogni catalogo di immagini (e il catalogo predefinito) può definire un set di profili ICC che costituiscono gli spazi di colore predefiniti per questo catalogo: uno in entrata e uno in uscita ciascuno per i dati in scala di grigio, RGB e CMYK. Vedi
[attributo::IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[attributo::IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[attributo::IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[attributo::IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[attributo::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[attributo::IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md).

## Spazio colore di ingresso {#section-9f08e2c1b6aa4fe4815be174972c1944}

Le immagini sorgente possono incorporare profili ICC per definire lo spazio colore di input. Se non è incorporato alcun profilo in un&#39;immagine sorgente, `attribute::IccProfileSrc*` del catalogo di immagini applicabile corrispondente al tipo di pixel dell&#39;immagine sorgente. Se questo attributo non è definito nel catalogo immagini, `attribute::IccProfile*` viene utilizzato. Se l’attributo di catalogo non è definito, l’immagine non è gestita tramite il colore e vengono applicate solo trasformazioni ingenue.

## Spazio colore di uscita {#section-b517bca622b64dcfa7defba6035d0716}

Lo spazio colore del risultato finale dell&#39;immagine di una richiesta è definito con `icc=` comando. Se `icc=` non è specificato, come spazio colore di output viene utilizzato lo spazio colore di output predefinito (dal catalogo principale della richiesta) che corrisponde al tipo di pixel dell&#39;immagine di output. Se non è definito alcun profilo di output nel catalogo principale o predefinito e se il livello base è un&#39;immagine con un profilo incorporato che corrisponde al tipo di pixel di output, tale profilo viene utilizzato per lo spazio colore di output. In caso contrario, lo spazio colore di output rimane indefinito: durante la conversione tra i tipi di pixel vengono applicate solo conversioni di colore ingenue e nell&#39;immagine di output non è possibile incorporare alcun profilo colore.

Lo spazio colore di output di una richiesta Image Serving nidificata/incorporata è sempre lo stesso dello spazio colore di output della richiesta di incorporamento esterna.

## Colori solidi {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Valori di colore specificati con `color=`, `bgcolor=`o il comando RTF `\iscolortbl` sono associati allo spazio colore di input se il valore del colore include il suffisso &quot;S&quot;, altrimenti sono associati allo spazio colore di output. Valori di colore specificati con `bgc=` o i comandi RTF `\colortbl` e `\cmykcolortbl` sono sempre associati allo spazio colore di output predefinito o effettivo corrispondente.

>[!NOTE]
>
>Al momento, `bgc=` non partecipa completamente alla gestione del colore. il suffisso &#39;S&#39; viene ignorato quando specificato con `bgc=`e la conversione ingenua viene applicata quando il tipo di pixel del valore del colore specificato con `bgc=` differisce dal tipo di pixel dell&#39;immagine di output. In caso contrario, `bgc=` è associato allo spazio colore di output effettivo.

## Richieste nidificate e incorporate {#section-bdda638c31504f26a77e51ebb1ea6e3b}

Lo spazio colore di output per le richieste IS nidificate e le richieste IR incorporate viene impostato automaticamente sullo spazio colore di output della richiesta più esterna, a meno che la richiesta nidificata non specifichi uno spazio colore di output esplicito con `icc=`. Inoltre, le richieste nidificate/incorporate ereditano anche gli spazi di colore di output predefiniti dal catalogo principale della richiesta più esterna, per garantire una gestione coerente dei valori di colore solido.

## Conversione dello spazio colore {#section-ca87b80b8e364ea59d8a92d87121b0fb}

Image Serving in genere tenta di ritardare le conversioni dei colori durante l&#39;elaborazione. Se tutti i livelli di un&#39;immagine hanno lo stesso spazio colore del livello, la conversione allo spazio colore di output viene eseguita dopo l&#39;unione e il ridimensionamento finale. Se sono coinvolti più spazi colore di livello, ogni livello viene trasformato nello spazio colore di output prima dell&#39;unione.

>[!NOTE]
>
>Comandi `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=`e `op_saturation=` sono operazioni RGB. Queste operazioni mantengono la fedeltà dei colori solo se lo spazio colore del livello è di tipo pixel RGB. Se non in RGB, i dati vengono convertiti in RGB utilizzando una conversione del colore ingenua e il risultato avrà una fedeltà del colore limitata. Lo spazio colore del livello per tali livelli deve essere considerato indeterminato.

Le opzioni di conversione del colore sono fornite con `icc=` o, se `icc=` non è specificato, con `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation`e `attribute::IccDither`.

## Incorporazione di profili di colore {#section-261ebbae5ce046589a776ca972380052}

Il profilo colore ICC dello spazio colore di output, se disponibile, può essere incorporato nell&#39;immagine di risposta specificando `iccEmbed=`.

## Gestione dei profili ICC {#section-eb210e4b44e64e2c8b80ee59216c5555}

Tutti i profili di colore utilizzati dal server devono essere conformi alla specifica ICC. I file di profilo ICC hanno in genere un [!DNL .icc] o [!DNL .icm] suffisso di file e si trovano in co-posizione con file di dati immagine.

Anche se i profili di output possono essere specificati dal percorso/nome del file nel `icc=` Si consiglia di registrare tutti i file di profilo nella Mappa del profilo ICC del catalogo o del catalogo di immagini predefiniti e di utilizzare gli identificatori di collegamento ( `icc::Name`) invece dei percorsi dei file.

Tutti i profili ICC a cui si fa riferimento in `catalog::IccProfile` e `attribute::IccProfile*` deve essere registrato nella mappa profilo ICC dell&#39;immagine o del catalogo predefinito.

## Restrizioni {#section-fb50ede40b124b89b30679da29782ab5}

Al momento sono supportati solo gli spazi colore CMYK, RGB e in scala di grigi.

## Profili colore ICC inclusi {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

Image Server include la maggior parte dei profili ICC standard di Adobe nel catalogo immagini predefinito. Questi profili sono accessibili dai loro nomi comuni (ad esempio, come mostrato in Photoshop) o con un identificatore leggermente più breve. Nella tabella seguente sono elencati tutti i profili ICC standard. Quando si fa riferimento a un profilo nella `icc=` gli spazi devono essere codificati come `%20`.

Puoi aggiungere altri profili ai profili standard, nel catalogo predefinito o in un catalogo di immagini specifico. Fai riferimento a [Riferimento alla mappa del profilo ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) per i dettagli.

>[!NOTE]
>
>La seguente tabella si applica a *Dynamic Media ibrido* solo (in esecuzione `dynamicmedia` modalità di esecuzione).

|Identificatore|Nome comune|Nome file| | | | | |**RGB**||| |`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc| |`AppleRGB`|Apple RGB|AppleRGB.icc| |`CIERGB`|CIE RGB|CIERGB.icc| |`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc| |`NTSC`NTSC (1953)|NTSC1953.icc| |`PAL`|PAL/SECAM|PAL_SECAM.icc| |`ProPhoto`|ProPhoto RGB|ProPhoto.icm| |`SMPTE`|SMPTE-C|SMPTE-C.icc| |`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profile.icm| |`WideGamutRGB`|Wide Gamut RGB|WideGamutRGB.icc| |**CMYK**||| |`CoatedFogra27`|FOGRA27 rivestito (ISO 12647-2:2004)|CoatedFOGRA27.icc| |`CoatedFogra39`|FOGRA39 rivestito (ISO 12647-2:2004)|CoatedFOGRA39.icc| |`CoatedGraCol`|GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc| |`EuropeISOCoated`|Europa ISO rivestito FOGRA27|EuropeISOCoatedFOGRA27.icc| |`EuroscaleCoated`|Euroscale rivestito|EuroscaleCoated.icc| |`EuroscaleUncoated`|Euroscale non rivestito v2|EuroscaleUnspato.icc| |`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc| |`JapanColorNewspaper`| Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc| |`JapanColorUncoated`|Giappone Colore 2001 non rivestito|JapanColor2001Non rivestito.icc| |`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc| |`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc| |`NewsprintSNAP2007`| Newsprint US (SNAP 2007)|USNewsprintSNAP2007.icc| |`PS4Default`|CMYK predefinito Photoshop 4|Photoshop4DefaultCMYK.icc| |`PS5Default`|CMYK predefinito Photoshop 5|Photoshop5DefaultCMYK.icc| |`SheetfedCoated`|USA Fogliame rivestito v2|USSheetfedCoated.icc| |`SheetfedUncoated`|USA Fogliame non rivestito v2|USSheetfedUnspalmato.icc| |`UncoatedFogra29`|FOGRA29 non rivestito (ISO 12647-2:2004)|FOGRA29.icc non rivestito| |`WebCoated`|USA Web Coated (SWOP) v2|USWebCoatedSWOP.icc| |`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc| |`WebCoatedGrade3`Carta SWOP 2006 di grado 3|Carta rivestita in web|WebCoatedSWOP2006Grade3.icc| |`WebCoatedGrade5`Carta SWOP 2006 di grado 5 | WebCoatedSWOP2006Grade5.icc| |`WebUncoated`|USA Web non rivestito v2|USWebUnsping.icc|

La seguente tabella si applica a *Dynamic Media Classic Image Serving* e *Dynamic Media* (in esecuzione `dynamicmedia_scene7` modalità di esecuzione).

|Identificatore|Nome comune|Nome file| | | | | |**RGB**||| |`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc| |`AppleRGB`|Apple RGB|AppleRGB.icc| |`CIERGB|CIE RGB`|CIERGB.icc| |`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc| |`NTSC`NTSC (1953)|NTSC1953.icc| |`PAL`|PAL/SECAM|PAL_SECAM.icc| |`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm| |`SMPTE`|SMPTE-C|SMPTE-C.icc| |`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profile.icm| |`WideGamutRGB`|Wide Gamut RGB|WideGamutRGB.icc| |**CMYK**||| |`CoatedFogra27`|FOGRA27 rivestito (ISO 12647-2:2004)|CoatedFOGRA27.icc| |`CoatedFogra39`|FOGRA39 rivestito (ISO 12647-2:2004)|CoatedFOGRA39.icc| |`Coated GRACoL 2006 (ISO 12647-2:2004)`|GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc| |`EuropeISOCoated`|Europa ISO rivestito FOGRA27|EuropeISOCoatedFOGRA27.icc| |`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc| |`EuroscaleUncoated`|Euroscale non rivestito v2|EuroscaleUnspato.icc| |`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc| |`JapanColorNewspaper`| Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc| |`JapanColorUncoated`|Giappone Colore 2001 non rivestito|JapanColor2001Non rivestito.icc| |`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc| |`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc| |`PS4Default`|CMYK predefinito Photoshop 4|Photoshop4DefaultCMYK.icc| |`PS5Default`|CMYK predefinito Photoshop 5|Photoshop5DefaultCMYK.icc| |`SheetfedCoated`|USA Fogliame rivestito v2|USSheetfedCoated.icc| |`SheetfedUncoated`|USA Fogliame non rivestito v2|USSheetfedUnspalmato.icc| |`UncoatedFogra29`|FOGRA29 non rivestito (ISO 12647-2:2004)|FOGRA29.icc non rivestito| |`US Newsprint (SNAP 2007)`| Newsprint US (SNAP 2007)|USNewsprintSNAP2007.icc| |`WebCoated`|USA Web Coated (SWOP) v2|USWebCoatedSWOP.icc| |`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc| |`Web Coated SWOP 2006 Grade 3 Paper`Carta SWOP 2006 di grado 3|Carta rivestita in web|WebCoatedSWOP2006Grade3.icc| |`Web Coated SWOP Grade 5 Paper`Carta SWOP 2006 di grado 5 | WebCoatedSWOP2006Grade5.icc| |`WebUncoated`|USA Web non rivestito v2|USWebUnsping.icc|

## Consultate anche {#section-39159397e80b4efca5f631eab8b9aa06}

[Consorzio internazionale del colore](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attributo::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;, [attributo::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;, [attributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attributo::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attributo::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [Riferimento alla mappa del profilo ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
