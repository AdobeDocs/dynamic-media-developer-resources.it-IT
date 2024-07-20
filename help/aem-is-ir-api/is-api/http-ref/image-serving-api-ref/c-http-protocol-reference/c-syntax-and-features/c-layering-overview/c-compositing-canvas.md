---
description: I livelli vengono composti nell'ordine specificato dal comando layer=, dove i livelli con numero più alto nascondono quelli con numero più basso.
solution: Experience Manager
title: Area di lavoro di composizione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Area di lavoro di composizione{#the-compositing-canvas}

I livelli vengono composti nell&#39;ordine specificato dal comando layer=, dove i livelli con numero più alto nascondono quelli con numero più basso.

Il livello 0 costituisce il livello di sfondo, che è sempre richiesto e che definisce le dimensioni dell&#39;immagine composita. Qualsiasi tipo di livello è consentito per il livello 0. La dimensione del livello 0 deve essere definita, in modo esplicito utilizzando `size=` o implicito, in base all&#39;immagine o al testo del contenuto. Le aree di altri livelli che non rientrano nell&#39;area del livello 0 non sono incluse nell&#39;immagine di output.

>[!NOTE]
>
>Una volta appiattiti tutti i livelli, l&#39;immagine composita viene convertita nell&#39;immagine di risposta finale, come specificato con i [comandi e gli attributi di visualizzazione](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
