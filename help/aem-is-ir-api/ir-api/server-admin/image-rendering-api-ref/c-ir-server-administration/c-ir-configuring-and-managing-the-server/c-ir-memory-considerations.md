---
description: La quantità di memoria utilizzata dal Image Rendering può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, poche vignette rispetto a molte vignette diverse, dimensioni e complessità delle vignette e così via).
solution: Experience Manager
title: Considerazioni sulla memoria
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# Considerazioni sulla memoria{#memory-considerations}

La quantità di memoria utilizzata dal Image Rendering può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, poche vignette rispetto a molte vignette diverse, dimensioni e complessità delle vignette e così via).

Per ottenere le migliori prestazioni, è necessario evitare il paging della memoria (scambio).

Image Rendering condivide la gestione della memoria di Image Server. Quando si utilizza Image Rendering, è necessario allocare ulteriore memoria. Il 30-50% della memoria fisica può essere ragionevole.

Per informazioni su come modificare l&#39;allocazione della memoria di Image Server (ImageServer::PhysicalMemory), fare riferimento alla documentazione di Image Server.
