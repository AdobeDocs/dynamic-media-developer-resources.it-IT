---
description: La quantità di memoria utilizzata da Image Rendering può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, vignettature poche e molte diverse, dimensioni e complessità delle vignettature e così via).
solution: Experience Manager
title: Considerazioni sulla memoria
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Considerazioni sulla memoria{#memory-considerations}

La quantità di memoria utilizzata da Image Rendering può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, vignettature poche e molte diverse, dimensioni e complessità delle vignettature e così via).

Per ottenere prestazioni ottimali, è necessario evitare il paging (scambio) della memoria.

Image Rendering condivide la gestione della memoria di Image Server. Quando si utilizza Image Rendering, è necessario allocare memoria aggiuntiva. Il 30-50% della memoria fisica può essere ragionevole.

Per informazioni su come modificare l&#39;allocazione della memoria del server immagini (ImageServer::PhysicalMemory), consultare la documentazione di Image Server.
