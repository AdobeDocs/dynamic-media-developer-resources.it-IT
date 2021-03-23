---
description: Stringa modificatore della richiesta di suffisso. Nessuno o più comandi Image Server separati dai caratteri '&'.
seo-description: Stringa modificatore della richiesta di suffisso. Nessuno o più comandi Image Server separati dai caratteri '&'.
seo-title: PostModifier
solution: Experience Manager
title: PostModifier
uuid: 8800a9b2-e9c0-498b-b4e1-37952ba7c842
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 4%

---


# PostModifier{#postmodifier}

Stringa modificatore della richiesta di suffisso. Nessuno o più comandi Image Server separati dai caratteri &#39;&amp;&#39;.

I comandi in questo campo sostituiscono sempre i comandi nella richiesta HTTP e in `catalog::Modifier`.

`catalog::PostModifier` è utile se alcune immagini richiedono impostazioni speciali normalmente controllate dall’URL, ad esempio  `qlt=` o  `resmode=`. `catalog::Modifier` deve essere utilizzato per impostare la maggior parte dei comandi IS nel catalogo immagini.

Le macro sono consentite in `catalog::PostModifier`, purché siano definite nello stesso catalogo o nel catalogo predefinito. È possibile utilizzare anche variabili personalizzate.

>[!NOTE]
>
>Se una richiesta coinvolge più livelli, viene applicato solo il contenuto di `catalog::PostModifier` del livello 0. `catalog::PostModifier` di tutti gli altri livelli viene ignorato.

## Proprietà {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Stringa di testo. Facoltativo.

## Predefinito {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Nessuno.

## Consultate anche {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalogo::Modificatore](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
