---
title: Supporto video esterno
description: Il visualizzatore supporta la riproduzione di video in hosting al di fuori di Dynamic Media Classic o Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Supporto video esterno{#external-video-support}

The viewer supports playing video hosted outside of Dynamic Media Classic or Adobe Experience Manager, Dynamic Media.

I formati supportati per il video esterno sono MP4 in formato H.264 o M3U8 manifest per il flusso HLS.

Il visualizzatore può lavorare con video Dynamic Media Classic o Experience Manager Dynamic Media o con video esterno. Se il visualizzatore inizia con un video Dynamic Media Classic/AEM Dynamic Media, deve essere utilizzato con tale tipo di risorsa che continua. Non è possibile caricare un video esterno in questo visualizzatore utilizzando il metodo [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) e viceversa. That is, if the viewer was initially loaded with external video, it continues to work with external videos only.

Quando si lavora con un video esterno, il visualizzatore ignora il valore di qualsiasi modificatore di riproduzione e rileva il tipo di riproduzione dall’estensione video esterna. Se l’URL del video esterno termina con `.m3u8`, il visualizzatore utilizza la riproduzione HLS; in caso contrario, viene utilizzata la riproduzione progressiva.
