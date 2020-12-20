---
description: I livelli sono composti nell’ordine specificato dal comando layer=, dove i livelli con numero superiore nascondono quelli con numero inferiore.
seo-description: I livelli sono composti nell’ordine specificato dal comando layer=, dove i livelli con numero superiore nascondono quelli con numero inferiore.
seo-title: Il quadro di composizione
solution: Experience Manager
title: Il quadro di composizione
topic: Scene7 Image Serving - Image Rendering API
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# Il quadro di composizione{#the-compositing-canvas}

I livelli sono composti nell’ordine specificato dal comando layer=, dove i livelli con numero superiore nascondono quelli con numero inferiore.

Il livello 0 costituisce il livello di sfondo, che è sempre richiesto e che definisce le dimensioni dell’immagine composita. Per il livello 0 è consentito qualsiasi tipo di livello. Le dimensioni del livello 0 devono essere definite, in modo esplicito utilizzando `size=` o implicitamente, in base all&#39;immagine o al testo del contenuto. Le aree di altri livelli che non rientrano nell’area del livello 0 non saranno incluse nell’immagine di output.

>[!NOTE]
>
>Dopo aver appiattito tutti i livelli, l&#39;immagine composita viene convertita nell&#39;immagine di risposta finale, come specificato con i comandi e gli attributi [view](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).

