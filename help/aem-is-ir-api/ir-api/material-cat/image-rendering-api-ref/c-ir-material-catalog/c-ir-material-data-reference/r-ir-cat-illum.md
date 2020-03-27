---
description: Selettore mappa di illuminazione. Consente una selezione esplicita della mappa di illuminazione da utilizzare per il rendering di questo materiale.
seo-description: Selettore mappa di illuminazione. Consente una selezione esplicita della mappa di illuminazione da utilizzare per il rendering di questo materiale.
seo-title: Illum
solution: Experience Manager
title: Illum
topic: Scene7 Image Serving - Image Rendering API
uuid: 2df0abbb-0d54-41b7-80c4-b914c18cd1b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Illum{#illum}

Selettore mappa di illuminazione. Consente una selezione esplicita della mappa di illuminazione da utilizzare per il rendering di questo materiale.

## Proprietà {#section-162bcf562ca844ccba9e81e267508cca}

Enum. Impostare su -1 per la selezione automatica della mappa di illuminazione in base al valore del catalogo::Gloss.

Impostare su 0, 1 o 2 per selezionare la mappa di illuminazione A, B o C. Il renderer sceglierà la mappa di illuminazione più vicina disponibile nella vignettatura.

## Predefinito {#section-ac386d31ef90423b8a367010a60bddc7}

-1 (selezione automatica)

## Consultate anche {#section-d9db8507a5e54692b84f54b3f84b782a}

[attributo::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)
