---
description: Il rendering delle immagini supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).
seo-description: Il rendering delle immagini supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).
seo-title: Gestione del colore del rendering delle immagini *
solution: Experience Manager
title: Gestione del colore del rendering delle immagini *
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c47f584-645f-4eb7-bdc0-fdef459da3b2
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# Gestione del colore del rendering delle immagini *{#image-rendering-color-management}

Il rendering delle immagini supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).

**Restrizioni**

Al momento sono supportati solo gli spazi colore CMYK, RGB e scala di grigi.

I file di stile Cabinet (.vnc) e i file di stile dei rivestimenti delle finestre ( [!DNL .vnw]) non sono gestiti a colori e si presume che esistano nello spazio colore di lavoro.

**Consultate anche**

[Consorzio](http://www.color.org/index.xalter) colori internazionale , [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , `attribute::IccBlackPointCompensation` , `attribute::IccDither` , Mappe profilo ICC

## Spazi colore predefiniti {#section-8ce27edf42e746febe4654f8f19b9c0c}

Ogni catalogo di immagini (e il catalogo predefinito) può definire un set di profili ICC. Questi profili costituiscono gli spazi colore predefiniti per questo catalogo: un input e un profilo di output ciascuno per i dati in scala di grigio, RGB e CMYK ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray`e `attribute::IccProfileSrcCmyk`).

Lo spazio colore predefinito per una particolare immagine o altro oggetto viene selezionato dai profili predefiniti del catalogo in base al tipo di pixel dell’immagine.

## Spazio colore ingresso {#section-660f661a7e954df4b451e34134195276}

Le immagini dei materiali possono incorporare profili ICC per definire lo spazio colore di input. Se non viene incorporato alcun profilo in un’immagine sorgente, verrà utilizzato `attribute::IccProfileSrc*` il catalogo di immagini applicabile corrispondente al tipo di pixel dell’immagine sorgente. Se questo attributo non è definito nel catalogo immagini, `attribute::IccProfile*` viene utilizzato. Se l’attributo del catalogo non è definito, l’immagine non viene gestita in base al colore e vengono applicate solo trasformazioni ingenue.

## Spazio colore di lavoro {#section-645d9cfa5b0347a190a0ece218f5b5e1}

In genere, lo spazio colore di lavoro è definito dal profilo colore ICC incorporato nella vignettatura. Se la vignettatura non include un profilo, per lo spazio colore di lavoro viene utilizzato il profilo di input RGB predefinito ( `attribute::IccProfileSrcRgb` del catalogo delle sessioni).

Tutte le operazioni di rendering vengono eseguite nello spazio colore di lavoro.

**Importante:** Il profilo ICC per lo spazio colore di lavoro deve supportare le trasformazioni di input e output. Se un profilo solo di output viene utilizzato come spazio colore di lavoro, l&#39;IR non sarà in grado di convertire i materiali in esso. Tale profilo colore può essere utilizzato anche se i materiali sono presenti nello stesso spazio colore di lavoro. Il tentativo di applicare materiali in altri spazi colore avrà esito negativo.

## Valori di colore espliciti {#section-31727bf1b23e477ca92572fbbf422d2f}

I valori di colore RGB specificati con `color=`, `bgc=`, `catalog::BgColor`e `catalog::Color` si presume siano presenti nello spazio colore di lavoro corrente.

## File di dati materiali {#section-33f7a170a6664c02b8479fb89cc0aea3}

I file immagine di materiale (texture e immagini decal) possono avere un tipo di pixel RGB, scala di grigi o CMYK e possono incorporare un profilo colore. Se non è incorporato alcun profilo colore, lo spazio colore di input predefinito è associato all&#39;immagine (ad esempio, il profilo colore dal catalogo dei materiali che corrisponde al tipo di pixel dell&#39;immagine).

Le immagini dei materiali ottenute da richieste nidificate di Image Server o di rendering delle immagini includono in genere un profilo colore. In caso contrario, le immagini sono associate allo spazio colore di input predefinito corrispondente al tipo di pixel.

Se lo spazio colore del file immagine è diverso dallo spazio colore di lavoro, per convertire nello spazio colore di lavoro viene utilizzata una conversione accurata dei colori. La conversione del tipo è utile quando non viene incorporato alcun profilo e non viene definito alcun profilo di input predefinito.

Altri file di dati di materiale, come i file di stile cabinet ( [!DNL .vnc]) o i file di copertura delle finestre ( [!DNL .vnw]), non incorporano profili colore e si presume sempre che siano nello spazio colore di lavoro.

## Spazio colore di output {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Tutte le operazioni di rendering vengono effettuate nello spazio colore di lavoro. Se la richiesta specifica un profilo colore diverso con il `icc=` comando, i dati verranno convertiti nello spazio colore appena prima che venga codificato e restituito al client. Quando la gestione del colore è disattivata, la conversione ingenua viene utilizzata se necessario per convertire in scala di grigio o CMYK.

## Profili colore incorporati {#section-5ff733832d38429fbe02b3c1e9bb94a9}

Il profilo colore associato all’immagine sottoposta a rendering può essere incorporato nell’immagine di risposta specificando `iccEmbed=` per la richiesta.

Se non `icc=` viene specificato, viene incorporato il profilo ICC per lo spazio colore di lavoro. Se la gestione del colore è disattivata e non è stato specificato alcun profilo con `icc=`.

## ICC, profili {#section-afeb76068b5042adb83261638e450140}

Tutti i profili colore utilizzati dal server devono essere conformi alle specifiche ICC. I file di profilo ICC hanno in genere un suffisso [!DNL .icc] o [!DNL .icm] file e si trovano in comune con i file di dati del materiale.

Mentre i profili di output possono essere specificati dal percorso/nome del file nel `icc=` comando, si consiglia di registrare tutti i file di profilo nella Mappa profilo ICC del catalogo predefinito o di un catalogo di materiali specifico e di utilizzare identificatori di scelta rapida ( `icc::Name`) invece dei percorsi di file.

I profili di lavoro devono essere registrati nella Mappa profilo ICC del catalogo dei materiali o del catalogo predefinito.
