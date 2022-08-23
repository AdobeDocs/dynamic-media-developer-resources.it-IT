---
title: TrustedDomains
description: Flash domini web dell'applicazione. Le applicazioni di Flash Adobe possono richiedere l'accesso alle proprietà delle immagini consegnate in formato swf. Il swf deve concedere l'accesso esplicitamente registrando il nome dei domini di applicazione di cui si fida.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---

# TrustedDomains{#trusteddomains}

Flash domini web dell&#39;applicazione. Le applicazioni di Flash Adobe possono richiedere l&#39;accesso alle proprietà delle immagini consegnate in formato swf. Il swf deve concedere l&#39;accesso esplicitamente registrando il nome dei domini di applicazione di cui si fida.

## Proprietà {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Stringa contenente un elenco separato da virgole di nomi di dominio web. Se vuoto, le applicazioni devono essere servite dallo stesso dominio del Image Rendering per poter accedere alle proprietà delle immagini in [!DNL swf]Risposte formattate.

## Predefinito {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Ereditato da `default::TrustedDomains` se non presente.

## Consultate anche {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attributo::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
