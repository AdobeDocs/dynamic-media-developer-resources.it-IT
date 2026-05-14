---
description: Stringa modificatore richiesta prefisso. Nessuno o più comandi Image Server separati da '&' caratteri.
solution: Experience Manager
title: Modificatore
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
TQID: 'https://experienceleague.adobe.com/b1j5WmY-PNOt1zW9qglJob5W8csmI3TidhDwoHK3kCM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 6%

---

# Modificatore{#modifier}

Stringa modificatore richiesta prefisso. Nessuno o più comandi Image Server separati da &#39;&amp;&#39; caratteri.

Utilizzato per modificare in modo persistente le immagini e memorizzare il corpo dei modelli.

I comandi in questo campo vengono sostituiti dagli stessi comandi nella richiesta o nel modello da cui si fa riferimento al record e dai comandi in `catalog::PostModifier`

Le macro sono consentite in `catalog::Modifier`, purché siano definite nello stesso catalogo o nel catalogo predefinito. È possibile utilizzare anche variabili personalizzate.

## Proprietà {#section-6674388f77d644469371a17e8809c45f}

Stringa di testo. Facoltativo.

## Predefinito {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Nessuno.

## Consultate anche {#section-7a67803d141b442180c418c1f3cff029}

[catalogo::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
