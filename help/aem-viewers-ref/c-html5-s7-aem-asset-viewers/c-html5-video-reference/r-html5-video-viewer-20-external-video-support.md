---
title: Supporto video esterno
description: Il visualizzatore supporta la riproduzione di video in hosting al di fuori di Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
TQID: 'https://experienceleague.adobe.com/HymmuAHcdNoNLbGyF0k0jo6ZQfIaPPEjy6w34GuNWZI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 0%

---

# Supporto video esterno{#external-video-support}

Il visualizzatore supporta la riproduzione di video in hosting al di fuori di Dynamic Media Classic o Adobe Experience Manager - Dynamic Media.

I formati supportati per il video esterno sono MP4 in formato H.264 o il manifesto M3U8 per il flusso HLS.

Il visualizzatore può lavorare con video Dynamic Media Classic o Experience Manager - Dynamic Media o con video esterno. Se il visualizzatore inizia con un video Dynamic Media Classic/Dynamic Media, utilizzalo con tale tipo di risorsa in futuro, non è possibile caricare un video esterno in questo visualizzatore utilizzando il metodo [`setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c). E viceversa: se l’utente inizialmente era caricato con un video esterno, dovrebbe continuare a lavorare solo con video esterni.

Quando si lavora con un video esterno, il visualizzatore ignora il valore del modificatore playback e rileva il tipo di riproduzione dall’estensione video esterna. Se l&#39;URL del video esterno termina con `.m3u8`, il visualizzatore utilizza la riproduzione HLS, altrimenti viene utilizzata la riproduzione progressiva.
