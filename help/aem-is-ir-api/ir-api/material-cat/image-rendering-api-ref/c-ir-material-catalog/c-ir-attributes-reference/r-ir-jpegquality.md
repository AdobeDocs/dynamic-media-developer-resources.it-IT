---
description: Qualità di codifica JPEG predefinita. Specifica l'impostazione di qualità predefinita per le immagini di risposta con codifica JPEG.
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 1a699a9e-dbf6-4e01-95aa-37a6eb83f4df
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# JpegQuality{#jpegquality}

Qualità di codifica JPEG predefinita. Specifica l&#39;impostazione di qualità predefinita per le immagini di risposta con codifica JPEG.

## Proprietà {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

Numero intero e flag, separati da una virgola. Il primo valore è compreso nell&#39;intervallo 1.100 e definisce la qualità. Il secondo valore può essere 0 per il comportamento normale, o 1 per disabilitare il sottocampionamento della cromaticità solitamente utilizzato dagli encoder JPEG.

## Predefinito {#section-60900c0fb8c54444b2361513232514db}

Ereditato da `default::JpegQuality` se non definito o se vuoto.

## Consultate anche {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
