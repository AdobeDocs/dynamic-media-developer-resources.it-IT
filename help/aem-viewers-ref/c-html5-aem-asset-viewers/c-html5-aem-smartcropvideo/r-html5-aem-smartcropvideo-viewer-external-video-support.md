---
title: Supporto video esterno
description: Il visualizzatore supporta la riproduzione di video in hosting al di fuori di Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
TQID: 'https://experienceleague.adobe.com/nLVjtwe8hj5YpMX6M1GKt1Fx-tZK2Qxe1kdWcK8BQPw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 0%

---

# Supporto video esterno{#external-video-support}

Il visualizzatore supporta la riproduzione di video in hosting al di fuori di Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.

I formati supportati per il video esterno sono MP4 in formato H.264 o il manifesto M3U8 per il flusso HLS.

Il visualizzatore può lavorare con video Dynamic Media Classic o Experience Manager - Dynamic Media o con video esterno. Se il visualizzatore inizia con un video Dynamic Media Classic/Dynamic Media, utilizzalo per tale tipo di risorsa, non è possibile caricare un video esterno in questo visualizzatore utilizzando [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) E viceversa: se l’utente inizialmente era caricato con un video esterno, dovrebbe continuare a lavorare solo con video esterni.

Quando si lavora con un video esterno, il visualizzatore ignora il valore del modificatore playback e rileva il tipo di riproduzione dall’estensione video esterna. Se l&#39;URL del video esterno termina con `.M3U8`, il visualizzatore utilizza la riproduzione HLS, altrimenti viene utilizzata la riproduzione progressiva.
