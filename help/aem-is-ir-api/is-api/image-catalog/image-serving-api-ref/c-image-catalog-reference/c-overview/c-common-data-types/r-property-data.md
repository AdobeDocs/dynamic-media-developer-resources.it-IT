---
description: I dati delle proprietà sono costituiti da una stringa di testo che rappresenta una o più proprietà.
solution: Experience Manager
title: Dati proprietà
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
TQID: 'https://experienceleague.adobe.com/jE8U1fgDsG9wdzG4O-BsPHvPOGLXDxZRMdZvL9LuYZE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 0%

---

# Dati proprietà{#property-data}

I dati delle proprietà sono costituiti da una stringa di testo che rappresenta una o più proprietà.

Una proprietà è costituita da un nome di proprietà e da un valore di proprietà, separati da =.

Più proprietà sono separate da separatori di riga, che possono essere `??` o `<CR><LF>`. Se l&#39;intera stringa di dati della proprietà non è racchiusa tra virgolette, il server sostituisce ogni occorrenza di `??` con `<CR><LF>` prima di trasmettere i dati al client. I nomi delle proprietà possono essere costituiti da lettere, numeri, &quot;.&quot;, &quot;-&quot; e &quot;_&quot;. I nomi delle proprietà non fanno distinzione tra maiuscole e minuscole.

I valori delle proprietà non devono includere separatori di riga.

Per ulteriori regole applicate ai dati delle proprietà, vedere [Stringa di testo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63).
