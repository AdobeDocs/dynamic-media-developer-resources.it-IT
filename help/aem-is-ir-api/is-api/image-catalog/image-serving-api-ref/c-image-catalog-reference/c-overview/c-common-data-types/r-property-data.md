---
description: I dati delle proprietà sono costituiti da una stringa di testo che rappresenta una o più proprietà.
solution: Experience Manager
title: Dati proprietà
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# Dati proprietà{#property-data}

I dati delle proprietà sono costituiti da una stringa di testo che rappresenta una o più proprietà.

Una proprietà è costituita da un nome di proprietà e da un valore di proprietà, separati da =.

Più proprietà sono separate da separatori di riga, che possono essere `??` o `<CR><LF>`. Se l&#39;intera stringa di dati della proprietà non è racchiusa tra virgolette, il server sostituisce ogni occorrenza di `??` con `<CR><LF>` prima di trasmettere i dati al client. I nomi delle proprietà possono essere costituiti da lettere, numeri, &quot;.&quot;, &quot;-&quot; e &quot;_&quot;. I nomi delle proprietà non fanno distinzione tra maiuscole e minuscole.

I valori delle proprietà non devono includere separatori di riga.

Consulta [Stringa di testo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) per regole aggiuntive applicate ai dati delle proprietà.
