---
description: I livelli sono composti nell'ordine specificato dal comando layer=, dove i livelli numerati più alti nascondono quelli numerati più in basso.
seo-description: I livelli sono composti nell'ordine specificato dal comando layer=, dove i livelli numerati più alti nascondono quelli numerati più in basso.
seo-title: Il quadro di composizione
solution: Experience Manager
title: Il quadro di composizione
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# Il quadro di composizione{#the-compositing-canvas}

I livelli sono composti nell&#39;ordine specificato dal comando layer=, dove i livelli numerati più alti nascondono quelli numerati più in basso.

Il livello 0 costituisce il livello di sfondo, che è sempre richiesto e che definisce le dimensioni dell&#39;immagine composita. Per il livello 0 è consentito qualsiasi tipo di livello. Le dimensioni del livello 0 devono essere definite, in modo esplicito utilizzando `size=` o implicitamente, in base all&#39;immagine o al testo del contenuto. Tutte le aree di altri livelli che non rientrano nell&#39;area del livello 0 non saranno incluse nell&#39;immagine di output.

>[!NOTE]
>
>Dopo che tutti i livelli sono appiattiti, l&#39;immagine composita viene convertita nell&#39;immagine di risposta finale, come specificato con i comandi e gli attributi [visualizza](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).

