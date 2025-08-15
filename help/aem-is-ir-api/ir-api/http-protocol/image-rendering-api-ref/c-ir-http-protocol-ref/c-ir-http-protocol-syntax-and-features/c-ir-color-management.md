---
description: Image Rendering supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).
solution: Experience Manager
title: Gestione colore Image Rendering*
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# Gestione colore Image Rendering*{#image-rendering-color-management}

Image Rendering supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).

**Limitazioni**

Al momento sono supportati solo gli spazi di colore CMYK, RGB e in scala di grigi.

I file di stile di scaffali (.vnc) e i file di stile delle finestre ( [!DNL .vnw]) non sono gestiti tramite colori e si presume che siano presenti nello spazio colore di lavoro.

**Vedere anche**

[International Color Consortium](https://www.color.org/index.xalter) , [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [`iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , `attribute::IccBlackPointCompensation` , `attribute::IccDither` , Mappe del profilo ICC

## Spazi colore predefiniti {#section-8ce27edf42e746febe4654f8f19b9c0c}

Ogni catalogo di immagini (e il catalogo predefinito) può definire un set di profili ICC. Questi profili costituiscono gli spazi colore predefiniti per questo catalogo: un profilo di input e un profilo di output ciascuno per i dati in scala di grigio, RGB e CMYK ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray` e `attribute::IccProfileSrcCmyk`).

Lo spazio colore predefinito per una particolare immagine o un altro oggetto viene selezionato dai profili predefiniti del catalogo in base al tipo di pixel dell’immagine.

## Spazio colore di input {#section-660f661a7e954df4b451e34134195276}

Le immagini dei materiali possono incorporare profili ICC per definire lo spazio colore di input. Se in un&#39;immagine di origine non è incorporato alcun profilo, viene utilizzato `attribute::IccProfileSrc*` del catalogo immagini applicabile corrispondente al tipo di pixel dell&#39;immagine di origine. Se questo attributo non è definito nel catalogo immagini, viene utilizzato `attribute::IccProfile*`. Se nemmeno l’attributo del catalogo è definito, l’immagine non viene gestita tramite colori e vengono applicate solo le trasformazioni naïve.

## Spazio colore di lavoro {#section-645d9cfa5b0347a190a0ece218f5b5e1}

In genere, lo spazio colore di lavoro è definito dal profilo colore ICC incorporato nella vignettatura. Se la vignettatura non include un profilo, per lo spazio colore di lavoro viene utilizzato il profilo di input RGB predefinito ( `attribute::IccProfileSrcRgb` del catalogo delle sessioni).

Tutte le operazioni di rendering vengono eseguite nello spazio colore di lavoro.

**Importante:** il profilo ICC per lo spazio colore di lavoro deve supportare le trasformazioni di input e output. Se viene utilizzato un profilo di solo output come spazio colore di lavoro, IR non è in grado di convertirvi i materiali. Tale profilo colore può essere ancora utilizzato se i materiali esistono nello stesso spazio colore di lavoro. Il tentativo di applicare materiali in altri spazi di colore non riesce.

## Valori colore espliciti {#section-31727bf1b23e477ca92572fbbf422d2f}

Si presume che i valori dei colori di RGB specificati con `color=`, `bgc=`, `catalog::BgColor` e `catalog::Color` siano presenti nello spazio colore di lavoro corrente.

## File di dati dei materiali {#section-33f7a170a6664c02b8479fb89cc0aea3}

I file di immagine di materiale (immagini di texture e decalcomanie) possono avere pixel RGB, in scala di grigi o CMYK e possono incorporare un profilo colore. Se non è incorporato alcun profilo colore, all&#39;immagine viene associato lo spazio colore di input predefinito, ad esempio il profilo colore del catalogo dei materiali che corrisponde al tipo di pixel dell&#39;immagine.

Le immagini di materiale ottenute da richieste di Image Server o Image Rendering nidificate in genere includono un profilo colore. In caso contrario, le immagini vengono associate allo spazio colore di input predefinito corrispondente al tipo di pixel.

Se lo spazio cromatico del file immagine è diverso da quello di lavoro, viene utilizzata una conversione accurata del colore per convertirlo nello spazio cromatico di lavoro. La conversione di tipo naïve viene utilizzata quando non è incorporato alcun profilo e non è definito alcun profilo di input predefinito.

Altri file di dati di materiale, ad esempio i file di stile archivio ( [!DNL .vnc]) o i file di copertina di finestre ( [!DNL .vnw]) non incorporano i profili colore e si presume che siano sempre nello spazio colore di lavoro.

## Spazio colore di output {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Tutte le operazioni di rendering vengono eseguite nello spazio colore di lavoro. Se la richiesta specifica un profilo colore diverso con il comando `icc=`, i dati vengono convertiti in tale spazio colore prima della codifica e restituiti al client. Quando la gestione del colore è disattivata, se necessario viene utilizzata una conversione naïve per la conversione in scala di grigi o CMYK.

## Profili colore incorporati {#section-5ff733832d38429fbe02b3c1e9bb94a9}

Il profilo colore associato all&#39;immagine di rendering può essere incorporato nell&#39;immagine di risposta specificando `iccEmbed=` per la richiesta.

Se `icc=` non è specificato, il profilo ICC per lo spazio colore di lavoro è incorporato. Nessun profilo incorporato se la gestione colore è disabilitata e non è stato specificato alcun profilo con `icc=`.

## Profili ICC {#section-afeb76068b5042adb83261638e450140}

Tutti i profili colore utilizzati dal server devono essere conformi alle specifiche ICC. I file di profilo ICC hanno in genere un suffisso di file [!DNL .icc] o [!DNL .icm] e si trovano in co-posizione con file di dati di materiale.

Sebbene i profili di output possano essere specificati in base al percorso/nome del file nel comando `icc=`, si consiglia di registrare tutti i file di profilo nella mappa dei profili ICC del catalogo predefinito o di un catalogo dei materiali specifico e di utilizzare gli identificatori di scelta rapida ( `icc::Name`) anziché i percorsi dei file.

I profili di lavoro devono essere registrati nella mappa dei profili ICC del catalogo dei materiali o del catalogo predefinito.
