---
description: Image Rendering supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).
solution: Experience Manager
title: Gestione del colore del rendering delle immagini *
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---


# Gestione del colore del rendering delle immagini *{#image-rendering-color-management}

Image Rendering supporta le conversioni dello spazio colore in base ai profili dello spazio colore conformi alle specifiche ICC (International Color Consortium).

**Restrizioni**

Al momento sono supportati solo gli spazi colore CMYK, RGB e in scala di grigi.

I file di stile Cabinet (.vnc) e i file di stile dei rivestimenti delle finestre ( [!DNL .vnw]) non sono gestiti dal colore e si presume che esistano nello spazio colore di lavoro.

**Consultate anche**

[Consorzio](http://www.color.org/index.xalter)  internazionale del colore,  [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) ,  [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) ,  `attribute::IccProfile*` ,  `attribute::IccProfileSrc*`,  `attribute::IccRenderIntent` ,  `attribute::IccBlackPointCompensation` ,  `attribute::IccDither` , Mappe del profilo ICC

## Spazi colore predefiniti {#section-8ce27edf42e746febe4654f8f19b9c0c}

Ogni catalogo di immagini (e il catalogo predefinito) può definire un set di profili ICC. Questi profili costituiscono gli spazi colore predefiniti per questo catalogo: uno in ingresso e un profilo di uscita ciascuno per i dati in scala di grigio, RGB e CMYK ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray` e `attribute::IccProfileSrcCmyk`).

Lo spazio colore predefinito per una particolare immagine o un altro oggetto viene selezionato dai profili predefiniti del catalogo in base al tipo di pixel dell’immagine.

## Spazio colore di ingresso {#section-660f661a7e954df4b451e34134195276}

Le immagini di materiale possono incorporare profili ICC per definire lo spazio colore di input. Se non è incorporato alcun profilo in un&#39;immagine sorgente, verrà utilizzato `attribute::IccProfileSrc*` del catalogo immagini applicabile corrispondente al tipo di pixel dell&#39;immagine sorgente. Se questo attributo non è definito nel catalogo immagini, viene utilizzato `attribute::IccProfile*`. Se l’attributo di catalogo non è definito, l’immagine non è gestita tramite il colore e vengono applicate solo trasformazioni ingenue.

## Spazio colore di lavoro {#section-645d9cfa5b0347a190a0ece218f5b5e1}

In genere, lo spazio colore di lavoro è definito dal profilo colore ICC incorporato nella vignetta. Se la vignetta non include un profilo, per lo spazio colore di lavoro viene utilizzato il profilo di ingresso RGB predefinito ( `attribute::IccProfileSrcRgb` del catalogo di sessione).

Tutte le operazioni di rendering vengono eseguite nello spazio colore di lavoro.

**Importante:** il profilo ICC per lo spazio colore di lavoro deve supportare le trasformazioni di input e output. Se un profilo di sola uscita viene utilizzato come spazio colore di lavoro, gli infrarossi non saranno in grado di convertire i materiali in esso. Tale profilo colore può essere ancora utilizzato se i materiali esistono nello stesso spazio colore di lavoro. Il tentativo di applicare materiali in altri spazi di colore avrà esito negativo.

## Valori di colore espliciti {#section-31727bf1b23e477ca92572fbbf422d2f}

I valori di colore RGB specificati con `color=`, `bgc=`, `catalog::BgColor` e `catalog::Color` sono considerati come presenti nello spazio colore di lavoro corrente.

## File di dati materiali {#section-33f7a170a6664c02b8479fb89cc0aea3}

I file immagine di materiale (texture e immagini decal) possono avere un tipo di pixel RGB, scala di grigi o CMYK e possono incorporare un profilo colore. Se non è incorporato alcun profilo colore, lo spazio colore di input predefinito è associato all&#39;immagine (ad esempio, il profilo colore dal catalogo del materiale che corrisponde al tipo di pixel dell&#39;immagine).

Le immagini dei materiali ottenute da richieste nidificate di Image Serving o Image Rendering generalmente includono un profilo colore. In caso contrario, le immagini sono associate allo spazio colore di input predefinito corrispondente al tipo di pixel.

Se lo spazio colore del file immagine è diverso dallo spazio colore di lavoro, per convertire nello spazio colore di lavoro viene utilizzata una conversione accurata dei colori. Viene utilizzata una conversione di tipo ingenuo quando non è incorporato alcun profilo e non è definito alcun profilo di input predefinito.

Altri file di dati di materiale, come i file di stile dell&#39;archivio ( [!DNL .vnc]) o i file di copertura della finestra ( [!DNL .vnw]), non incorporano profili di colore e si presume sempre che siano nello spazio colore di lavoro.

## Spazio colore di uscita {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Tutte le operazioni di rendering hanno luogo nello spazio colore di lavoro. Se la richiesta specifica un profilo colore diverso con il comando `icc=`, i dati verranno convertiti in tale spazio colore poco prima che venga codificato e restituito al client. Quando la gestione del colore è disabilitata, la conversione ingenua viene utilizzata se necessario per convertire in scala di grigi o CMYK.

## Profili colore incorporati {#section-5ff733832d38429fbe02b3c1e9bb94a9}

Il profilo colore associato all’immagine renderizzata può essere incorporato nell’immagine di risposta specificando `iccEmbed=` per la richiesta.

Se `icc=` non è specificato, viene incorporato il profilo ICC per lo spazio colore di lavoro. Se la gestione del colore è disabilitata e non è stato specificato alcun profilo con `icc=`, non viene incorporato alcun profilo.

## ICC, profili {#section-afeb76068b5042adb83261638e450140}

Tutti i profili di colore utilizzati dal server devono essere conformi alla specifica ICC. I file di profilo ICC hanno in genere un suffisso di file [!DNL .icc] o [!DNL .icm] e si trovano in co-posizione con file di dati di materiale.

Mentre i profili di output possono essere specificati dal percorso/nome del file nel comando `icc=`, si consiglia di registrare tutti i file di profilo nella Mappa del profilo ICC del catalogo predefinito o di un catalogo di materiali specifico e di utilizzare identificatori di scelta rapida ( `icc::Name`) invece dei percorsi dei file.

I profili di lavoro devono essere registrati nella mappa profilo ICC del catalogo dei materiali o del catalogo predefinito.
