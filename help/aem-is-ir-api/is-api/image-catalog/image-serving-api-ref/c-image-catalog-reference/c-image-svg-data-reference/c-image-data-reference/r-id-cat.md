---
description: Identificatore del record del catalogo
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---


# ID {#id}

Valore chiave di indice in base al quale i record nel file di dati immagine vengono cercati dal server Platform.

In genere, un identificatore immagine breve e univoco, ad esempio un numero SKU, probabilmente con un suffisso immagine, se un SKU ha più immagini. Può anche essere una stringa più complessa che assomiglia più a un percorso di file, per supportare un facile adattamento di siti web con Image Serving.

## Proprietà {#id-properties}

Stringa di testo. Obbligatorio. Chiave indice principale per la tabella dati immagine. Ogni valore catalog::Id deve essere univoco all’interno della tabella.

## Predefinito {#id-default}

Nessuno.

## Consultate anche {#id-seealso}

[attributo::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)