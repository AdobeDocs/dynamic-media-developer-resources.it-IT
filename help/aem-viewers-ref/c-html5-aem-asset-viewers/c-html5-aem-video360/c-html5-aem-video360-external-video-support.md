---
description: Il visualizzatore supporta la riproduzione di video in hosting all’esterno di SPS o AEM Dynamic Media.
seo-description: Il visualizzatore supporta la riproduzione di video in hosting all’esterno di SPS o AEM Dynamic Media.
seo-title: Supporto video esterno
solution: Experience Manager
title: Supporto video esterno
topic: Dynamic media
uuid: 2e9f1c54-627f-4462-ae85-8a5ca1d09762
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Supporto video esterno{#external-video-support}

Il visualizzatore supporta la riproduzione di video in hosting all’esterno di SPS o AEM Dynamic Media.

I formati supportati per il video esterno sono MP4 in formato H.264 o M3U8 manifest per il flusso HLS.

Il visualizzatore può utilizzare video Dynamic Media Classic o AEM Dynamic Media o con video esterni. Se il visualizzatore inizia con video Dynamic Media Classic/AEM Dynamic Media, deve essere utilizzato con il tipo di risorsa in corso. Non è possibile caricare un video esterno in questo visualizzatore con il metodo [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) e viceversa. Se il visualizzatore è stato inizialmente caricato con video esterni, continua a funzionare solo con video esterni.

Quando lavorate con un video esterno, il visualizzatore ignora il valore di qualsiasi modificatore di riproduzione e rileva il tipo di riproduzione dall’estensione video esterna. Se l’URL del video esterno termina con `.m3u8`, il visualizzatore utilizza la riproduzione HLS; in caso contrario, viene utilizzata la riproduzione progressiva.
