---
description: I livelli vengono composti nell'ordine specificato dal comando layer=, dove i livelli con numero più alto nascondono quelli con numero più basso.
solution: Experience Manager
title: Area di lavoro di composizione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
TQID: 'https://experienceleague.adobe.com/WNvq6dLRetz3iEbtP0ugmOPagUfTCaa5eXdB3lEzEaQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 0%

---

# Area di lavoro di composizione{#the-compositing-canvas}

I livelli vengono composti nell&#39;ordine specificato dal comando layer=, dove i livelli con numero più alto nascondono quelli con numero più basso.

Il livello 0 costituisce il livello di sfondo, che è sempre richiesto e che definisce le dimensioni dell&#39;immagine composita. Qualsiasi tipo di livello è consentito per il livello 0. La dimensione del livello 0 deve essere definita, in modo esplicito utilizzando `size=` o implicito, in base all&#39;immagine o al testo del contenuto. Le aree di altri livelli che non rientrano nell&#39;area del livello 0 non sono incluse nell&#39;immagine di output.

>[!NOTE]
>
>Una volta appiattiti tutti i livelli, l&#39;immagine composita viene convertita nell&#39;immagine di risposta finale, come specificato con i [comandi e gli attributi di visualizzazione](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
