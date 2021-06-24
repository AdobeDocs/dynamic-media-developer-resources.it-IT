---
description: Il visualizzatore supporta la riproduzione di video in hosting al di fuori di Dynamic Media Classic o AEM Dynamic Media.
solution: Experience Manager
title: Supporto video esterno
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video
role: Developer,Business Practitioner
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Supporto video esterno{#external-video-support}

Il visualizzatore supporta la riproduzione di video in hosting al di fuori di Dynamic Media Classic o AEM Dynamic Media.

I formati supportati per il video esterno sono MP4 in formato H.264 o M3U8 manifest per il flusso HLS.

Il visualizzatore può funzionare sia con video Dynamic Media Classic o AEM Dynamic Media che con video esterno. Se il visualizzatore inizia con un video Dynamic Media Classic/Dynamic Media, utilizzalo con tale tipo di risorsa in futuro, non è possibile caricare un video esterno in questo visualizzatore utilizzando il metodo [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) . E verso vizio: se il visualizzatore è stato inizialmente caricato con video esterni, dovrebbe continuare a lavorare solo con video esterni.

Quando si lavora con un video esterno, il visualizzatore ignora il valore del modificatore di riproduzione e rileva il tipo di riproduzione dall’estensione video esterna. Se l’URL video esterno termina con .m3u8, il visualizzatore utilizza la riproduzione HLS, altrimenti viene utilizzata la riproduzione progressiva.
