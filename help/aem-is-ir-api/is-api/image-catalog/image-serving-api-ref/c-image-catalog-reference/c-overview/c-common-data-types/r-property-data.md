---
description: I dati delle proprietà sono costituiti da una stringa di testo che rappresenta una o più proprietà.
seo-description: I dati delle proprietà sono costituiti da una stringa di testo che rappresenta una o più proprietà.
seo-title: Dati proprietà
solution: Experience Manager
title: Dati proprietà
topic: Scene7 Image Serving - Image Rendering API
uuid: 7fa6ae70-8d70-41d6-9e47-7df3d616874c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# Dati proprietà{#property-data}

I dati delle proprietà sono costituiti da una stringa di testo che rappresenta una o più proprietà.

Una proprietà è costituita da un nome di proprietà e un valore di proprietà, separati da =.

Più proprietà sono separate da separatori di riga, che possono essere `??` o `<CR><LF>`. Se l&#39;intera stringa di dati della proprietà non è racchiusa tra virgolette, il server sostituisce ogni occorrenza di `??` con `<CR><LF>` prima di trasmettere i dati al client. I nomi delle proprietà possono essere lettere, numeri, &#39;.&#39;, &#39;-&#39; e &#39;_&#39;. I nomi delle proprietà non fanno distinzione tra maiuscole e minuscole.

I valori delle proprietà non devono includere separatori di riga.

Per ulteriori regole applicate ai dati delle proprietà, vedere [Stringa di testo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63).
