---
description: La quantità di memoria utilizzata da Image Rendering può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, vignettature poche e molte diverse, dimensioni e complessità delle vignettature e così via).
solution: Experience Manager
title: Considerazioni sulla memoria
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
TQID: 'https://experienceleague.adobe.com/l41dx4mMn82TvImVVCJJKgJZbP-mWT5KbnzfZ5xFJqg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 129
ht-degree: 0%

---

# Considerazioni sulla memoria{#memory-considerations}

La quantità di memoria utilizzata da Image Rendering può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, vignettature poche e molte diverse, dimensioni e complessità delle vignettature e così via).

Per ottenere prestazioni ottimali, è necessario evitare il paging (scambio) della memoria.

Image Rendering condivide la gestione della memoria di Image Server. Quando si utilizza Image Rendering, è necessario allocare memoria aggiuntiva. Il 30-50% della memoria fisica può essere ragionevole.

Per informazioni su come modificare l&#39;allocazione della memoria del server immagini (ImageServer::PhysicalMemory), consultare la documentazione di Image Server.
