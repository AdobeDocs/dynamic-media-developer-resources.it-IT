---
description: I dati della proprietà sono costituiti da una stringa di testo che rappresenta una o più proprietà.
seo-description: I dati della proprietà sono costituiti da una stringa di testo che rappresenta una o più proprietà.
seo-title: Dati proprietà
solution: Experience Manager
title: Dati proprietà
uuid: 7fa6ae70-8d70-41d6-9e47-7df3d616874c
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---


# Dati proprietà{#property-data}

I dati della proprietà sono costituiti da una stringa di testo che rappresenta una o più proprietà.

Una proprietà è costituita da un nome di proprietà e un valore di proprietà, separati da =.

Le proprietà multiple sono separate da separatori di riga, che possono essere `??` o `<CR><LF>`. Se l&#39;intera stringa di dati della proprietà non è racchiusa tra virgolette, il server sostituisce ogni occorrenza di `??` con `<CR><LF>` prima di trasmettere i dati al client. I nomi delle proprietà possono essere costituiti da lettere, numeri, &#39;.&#39;, &#39;-&#39; e &#39;_&#39;. I nomi delle proprietà non fanno distinzione tra maiuscole e minuscole.

I valori di proprietà non devono includere separatori di riga.

Per ulteriori regole applicate ai dati di proprietà, consulta [Stringa di testo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) .
