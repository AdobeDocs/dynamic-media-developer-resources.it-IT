---
description: Il visualizzatore supporta la riproduzione di video in hosting all'esterno di Scene7 Publishing System o AEM Dynamic Media.
seo-description: Il visualizzatore supporta la riproduzione di video in hosting all'esterno di Scene7 Publishing System o AEM Dynamic Media.
seo-title: Supporto video esterno
solution: Experience Manager
title: Supporto video esterno
topic: Dynamic media
uuid: 24739a5a-3a5d-49b8-9a15-bcf3a95fc192
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# Supporto per video esterni{#external-video-support}

Il visualizzatore supporta la riproduzione di video in hosting all&#39;esterno di Scene7 Publishing System o AEM Dynamic Media.

I formati supportati per il video esterno sono MP4 in formato H.264 o M3U8 manifest per il flusso HLS.

Il visualizzatore può utilizzare video Scene7 o Dynamic Media o con video esterni. Se il visualizzatore inizia con video Scene7/Dynamic Media, usatelo con tale tipo di risorsa in futuro, non sarà possibile caricare un video esterno in questo visualizzatore utilizzando il metodo [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). E verso vizio: se il visualizzatore è stato inizialmente caricato con video esterni, dovrebbe continuare a lavorare solo con video esterni.

Quando lavorate con un video esterno, il visualizzatore ignora il valore del modificatore di riproduzione e rileva il tipo di riproduzione dall’estensione video esterna. Se l’URL del video esterno termina con .m3u8, il visualizzatore utilizza la riproduzione HLS, in caso contrario viene utilizzata la riproduzione progressiva.
