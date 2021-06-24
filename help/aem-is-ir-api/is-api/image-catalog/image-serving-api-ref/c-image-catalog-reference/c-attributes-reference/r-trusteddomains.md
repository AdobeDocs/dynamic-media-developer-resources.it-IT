---
description: Flash domini web dell'applicazione. Le applicazioni di Flash di Adobe possono richiedere l'accesso alle proprietà delle immagini fornite con fmt=swf o fmt=swf3.
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---

# TrustedDomains{#trusteddomains}

Flash domini web dell&#39;applicazione. Le applicazioni di Flash di Adobe possono richiedere l&#39;accesso alle proprietà delle immagini fornite con fmt=swf o fmt=swf3.

Il swf deve concedere l&#39;accesso esplicitamente registrando il nome dei domini di applicazione di cui si fida.

## Proprietà {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Stringa contenente un elenco separato da virgole di nomi di dominio web. Se vuoto, le applicazioni devono essere servite dallo stesso dominio di Image Rendering per poter accedere alle proprietà delle immagini nelle risposte in formato swf.

## Predefinito {#section-5c52ed3c7310488380f5a6f9540bf981}

Ereditato da `default::TrustedDomains` se non presente.

## Consultate anche {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
