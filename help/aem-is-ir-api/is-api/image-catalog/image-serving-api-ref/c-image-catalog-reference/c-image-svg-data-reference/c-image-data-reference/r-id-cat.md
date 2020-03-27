---
description: Identificatore record catalogo
solution: Experience Manager
title: ID
topic: Scene7 Image Serving - Image Rendering API
uuid: 9803d754-1f94-4e5d-9a40-3936676c0035
translation-type: tm+mt
source-git-commit: 7d3902803d42f5d479dd04ac9470a4088809f3d6

---


# ID {#id}

Valore chiave indice tramite il quale i record nel file di dati immagine vengono cercati dal server piattaforma.

In genere, un identificatore immagine breve e univoco, ad esempio un numero SKU, con un possibile suffisso immagine, se uno SKU ha più immagini. Può trattarsi anche di una stringa più complessa che assomiglia maggiormente a un percorso di file, per facilitare l’adattamento dei siti Web con Image Server.

## Proprietà {#id-properties}

Stringa di testo. Obbligatorio. Chiave di indice principale per la tabella di dati immagine. Ogni valore catalogo::Id deve essere univoco all’interno della tabella.

## Predefinito {#id-default}

Nessuno.

## Consultate anche {#id-seealso}

[attributo::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)