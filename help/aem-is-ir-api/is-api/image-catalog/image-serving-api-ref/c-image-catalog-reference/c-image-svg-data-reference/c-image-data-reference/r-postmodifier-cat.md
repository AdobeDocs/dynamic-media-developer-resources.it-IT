---
description: Stringa modificatore richiesta suffisso. Nessuno o più comandi Image Server separati dai caratteri '&'.
seo-description: Stringa modificatore richiesta suffisso. Nessuno o più comandi Image Server separati dai caratteri '&'.
seo-title: PostModifier
solution: Experience Manager
title: PostModifier
topic: Scene7 Image Serving - Image Rendering API
uuid: 8800a9b2-e9c0-498b-b4e1-37952ba7c842
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PostModifier{#postmodifier}

Stringa modificatore richiesta suffisso. Nessuno o più comandi Image Server separati dai caratteri &#39;&amp;&#39;.

I comandi in questo campo sovrascrivono sempre i comandi nella richiesta HTTP e in `catalog::Modifier`.

`catalog::PostModifier` è utile se alcune immagini richiedono impostazioni speciali che vengono normalmente controllate dall’URL, ad esempio `qlt=` o `resmode=`. `catalog::Modifier` deve essere utilizzato per impostare la maggior parte dei comandi IS nel catalogo immagini.

Le macro sono consentite in `catalog::PostModifier`, purché siano definite nello stesso catalogo o nel catalogo predefinito. È possibile utilizzare anche variabili personalizzate.

>[!NOTE]
>
>Se una richiesta interessa più livelli, viene applicato solo il contenuto del livello 0 `catalog::PostModifier` di livello. `catalog::PostModifier` di tutti gli altri livelli viene ignorato.

## Proprietà {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Stringa di testo. Facoltativo.

## Predefinito {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Nessuno.

## Consultate anche {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalogo:Modificatore](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
