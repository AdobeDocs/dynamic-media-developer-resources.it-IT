---
description: La quantità di memoria utilizzata dal rendering delle immagini può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, poche vignettature rispetto a molte altre, dimensioni e complessità delle vignettature, e così via).
seo-description: La quantità di memoria utilizzata dal rendering delle immagini può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, poche vignettature rispetto a molte altre, dimensioni e complessità delle vignettature, e così via).
seo-title: Considerazioni sulla memoria
solution: Experience Manager
title: Considerazioni sulla memoria
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 21247081-ff27-4237-93da-5fc996417dfd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# Considerazioni sulla memoria{#memory-considerations}

La quantità di memoria utilizzata dal rendering delle immagini può variare notevolmente e dipende in larga misura dal carico e dall’utilizzo effettivi del server (ad esempio, poche vignettature rispetto a molte altre, dimensioni e complessità delle vignettature, e così via).

Per ottenere prestazioni ottimali, è necessario evitare il paging della memoria (scambio di dati).

Image Rendering condivide la gestione della memoria del server immagini. Quando si utilizza il rendering delle immagini, occorre allocare ulteriore memoria. Il 30-50% della memoria fisica può essere ragionevole.

Per informazioni su come modificare l’allocazione di memoria del server immagini (ImageServer::PhysicalMemory), consultate la documentazione di Image Server.
