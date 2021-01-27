---
description: Il visualizzatore supporta la riproduzione di video in hosting all'esterno di Dynamic Media Classic o AEM Dynamic Media.
solution: Experience Manager
title: Supporto video esterno
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Supporto per video esterni{#external-video-support}

Il visualizzatore supporta la riproduzione di video in hosting all&#39;esterno di Dynamic Media Classic o AEM Dynamic Media.

I formati supportati per il video esterno sono MP4 in formato H.264 o M3U8 manifest per il flusso HLS.

Il visualizzatore può lavorare su video Dynamic Media Dynamic Media Classic o AEM oppure con video esterni. Se il visualizzatore inizia con un video Dynamic Media Dynamic Media Classic/AEM, deve essere utilizzato con tale tipo di risorsa per il futuro. Non è possibile caricare un video esterno in questo visualizzatore utilizzando il metodo [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) e viceversa. Se il visualizzatore è stato inizialmente caricato con video esterni, continua a funzionare solo con video esterni.

Quando lavorate con un video esterno, il visualizzatore ignora il valore di qualsiasi modificatore di riproduzione e rileva il tipo di riproduzione dall’estensione video esterna. Se l&#39;URL del video esterno termina con `.m3u8`, il visualizzatore utilizza la riproduzione HLS; in caso contrario, viene utilizzata la riproduzione progressiva.
