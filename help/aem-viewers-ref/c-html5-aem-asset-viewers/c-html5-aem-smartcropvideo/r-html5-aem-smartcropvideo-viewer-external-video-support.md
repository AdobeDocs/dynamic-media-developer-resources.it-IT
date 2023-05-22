---
title: Supporto video esterno
description: Il visualizzatore supporta la riproduzione di video in hosting al di fuori di Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Supporto video esterno{#external-video-support}

Il visualizzatore supporta la riproduzione di video in hosting al di fuori di Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.

I formati supportati per il video esterno sono MP4 in formato H.264 o il manifesto M3U8 per lo streaming HLS.

Il visualizzatore può lavorare con Dynamic Media Classic o con video Dynamic Media Experience Manager o con video esterni. Se il visualizzatore inizia con un video Dynamic Media Classic/Dynamic Media, utilizzalo con tale tipo di risorsa per il futuro, non è possibile caricare un video esterno in questo visualizzatore utilizzando [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) E viceversa: se l’utente inizialmente era caricato con un video esterno, dovrebbe continuare a lavorare solo con video esterni.

Quando si lavora con un video esterno, il visualizzatore ignora il valore del modificatore playback e rileva il tipo di riproduzione dall’estensione video esterna. Se l’URL del video esterno termina con `.M3U8` il visualizzatore utilizza la riproduzione HLS, altrimenti viene utilizzata la riproduzione progressiva.
