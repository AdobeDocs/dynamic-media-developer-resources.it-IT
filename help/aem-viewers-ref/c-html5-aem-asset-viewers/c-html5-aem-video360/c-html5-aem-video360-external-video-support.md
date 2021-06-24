---
description: Il visualizzatore supporta la riproduzione di video in hosting al di fuori di Dynamic Media Classic o AEM Dynamic Media.
solution: Experience Manager
title: Supporto video esterno
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video VR 360
role: Developer,Business Practitioner
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# Supporto video esterno{#external-video-support}

Il visualizzatore supporta la riproduzione di video in hosting al di fuori di Dynamic Media Classic o AEM Dynamic Media.

I formati supportati per il video esterno sono MP4 in formato H.264 o M3U8 manifest per il flusso HLS.

Il visualizzatore può funzionare sia con video Dynamic Media Classic o AEM Dynamic Media che con video esterno. Se il visualizzatore inizia con un video Dynamic Media Classic/AEM Dynamic Media, deve essere utilizzato con tale tipo di risorsa in futuro. Non è possibile caricare un video esterno in questo visualizzatore utilizzando il metodo [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) e viceversa. In altre parole, se il visualizzatore è stato inizialmente caricato di video esterni, continua a funzionare solo con video esterni.

Quando si lavora con un video esterno, il visualizzatore ignora il valore di qualsiasi modificatore di riproduzione e rileva il tipo di riproduzione dall’estensione video esterna. Se l’URL del video esterno termina con `.m3u8`, il visualizzatore utilizza la riproduzione HLS; in caso contrario, viene utilizzata la riproduzione progressiva.
