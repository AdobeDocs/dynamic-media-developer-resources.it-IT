---
description: Stringa modificatore della richiesta di suffisso. Nessuno o più comandi Image Server separati dai caratteri '&'.
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '132'
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
