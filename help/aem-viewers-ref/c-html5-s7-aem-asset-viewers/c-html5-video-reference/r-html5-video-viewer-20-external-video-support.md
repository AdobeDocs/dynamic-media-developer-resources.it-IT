---
title: Supporto video esterno
description: Il visualizzatore supporta la riproduzione di video in hosting al di fuori di Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# Supporto video esterno{#external-video-support}

Il visualizzatore supporta la riproduzione di video in hosting al di fuori di Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.

I formati supportati per il video esterno sono MP4 in formato H.264 o il manifesto M3U8 per il flusso HLS.

Il visualizzatore può lavorare con video Dynamic Media Classic o Experience Manager - Dynamic Media o con video esterno. Se il visualizzatore inizia con un video Dynamic Media Classic/Dynamic Media, utilizzalo con tale tipo di risorsa in futuro, non è possibile caricare un video esterno in questo visualizzatore utilizzando il metodo [`setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). E viceversa: se l’utente inizialmente era caricato con un video esterno, dovrebbe continuare a lavorare solo con video esterni.

Quando si lavora con un video esterno, il visualizzatore ignora il valore del modificatore playback e rileva il tipo di riproduzione dall’estensione video esterna. Se l&#39;URL del video esterno termina con `.m3u8`, il visualizzatore utilizza la riproduzione HLS, altrimenti viene utilizzata la riproduzione progressiva.
