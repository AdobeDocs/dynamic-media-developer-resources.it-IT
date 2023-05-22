---
description: I livelli vengono composti nell'ordine specificato dal comando layer=, dove i livelli con numero più alto nascondono quelli con numero più basso.
solution: Experience Manager
title: Area di lavoro di composizione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Area di lavoro di composizione{#the-compositing-canvas}

I livelli vengono composti nell&#39;ordine specificato dal comando layer=, dove i livelli con numero più alto nascondono quelli con numero più basso.

Il livello 0 costituisce il livello di sfondo, che è sempre richiesto e che definisce le dimensioni dell&#39;immagine composita. Qualsiasi tipo di livello è consentito per il livello 0. È necessario definire la dimensione del livello 0, utilizzando esplicitamente `size=` o implicitamente, in base all’immagine o al testo del contenuto. Eventuali aree di altri livelli che non rientrano nell&#39;area del livello 0 non verranno incluse nell&#39;immagine di output.

>[!NOTE]
>
>Una volta appiattiti tutti i livelli, l&#39;immagine composita viene convertita nell&#39;immagine di risposta finale, come specificato con [visualizzare comandi e attributi](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
