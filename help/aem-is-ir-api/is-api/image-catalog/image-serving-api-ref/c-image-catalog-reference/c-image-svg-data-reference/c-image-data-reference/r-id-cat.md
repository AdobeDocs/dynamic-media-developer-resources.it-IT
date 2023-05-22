---
description: Identificatore record catalogo
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 5%

---

# ID {#id}

Valore chiave dell&#39;indice in base al quale i record nel file di dati immagine vengono cercati dal [!DNL Platform Server].

In genere, se una SKU ha più immagini, si tratta di un identificatore immagine breve e univoco, ad esempio un numero SKU, che può anche contenere una sorta di suffisso immagine. Può anche essere una stringa più complessa, più simile a un percorso di file, per supportare una facile installazione retroattiva dei siti web con Image Server.

## Proprietà {#id-properties}

Stringa di testo. Obbligatorio. Chiave di indice primaria per la tabella dati immagine. Ogni valore catalog::Id deve essere univoco all&#39;interno della tabella.

## Predefinito {#id-default}

Nessuno.

## Consultate anche {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
