---
description: La quantità di memoria utilizzata dal Image Rendering può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, poche vignette rispetto a molte vignette diverse, dimensioni e complessità delle vignette e così via).
seo-description: La quantità di memoria utilizzata dal Image Rendering può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, poche vignette rispetto a molte vignette diverse, dimensioni e complessità delle vignette e così via).
seo-title: Considerazioni sulla memoria
solution: Experience Manager
title: Considerazioni sulla memoria
uuid: 21247081-ff27-4237-93da-5fc996417dfd
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Considerazioni sulla memoria{#memory-considerations}

La quantità di memoria utilizzata dal Image Rendering può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, poche vignette rispetto a molte vignette diverse, dimensioni e complessità delle vignette e così via).

Per ottenere le migliori prestazioni, è necessario evitare il paging della memoria (scambio).

Image Rendering condivide la gestione della memoria di Image Server. Quando si utilizza Image Rendering, è necessario allocare ulteriore memoria. Il 30-50% della memoria fisica può essere ragionevole.

Per informazioni su come modificare l&#39;allocazione della memoria di Image Server (ImageServer::PhysicalMemory), fare riferimento alla documentazione di Image Server.
