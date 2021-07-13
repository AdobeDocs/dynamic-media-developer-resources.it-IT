---
description: La quantità di memoria utilizzata dal Image Rendering può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, poche vignette rispetto a molte vignette diverse, dimensioni e complessità delle vignette e così via).
solution: Experience Manager
title: Considerazioni sulla memoria
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Considerazioni sulla memoria{#memory-considerations}

La quantità di memoria utilizzata dal Image Rendering può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, poche vignette rispetto a molte vignette diverse, dimensioni e complessità delle vignette e così via).

Per ottenere le migliori prestazioni, è necessario evitare il paging della memoria (scambio).

Image Rendering condivide la gestione della memoria di Image Server. Quando si utilizza Image Rendering, è necessario allocare ulteriore memoria. Il 30-50% della memoria fisica può essere ragionevole.

Per informazioni su come modificare l&#39;allocazione della memoria di Image Server (ImageServer::PhysicalMemory), fare riferimento alla documentazione di Image Server.
