---
description: Flash domini web dell'applicazione. Le applicazioni di Flash di Adobe possono richiedere l'accesso alle proprietà delle immagini fornite con fmt=swf o fmt=swf3.
seo-description: Flash domini web dell'applicazione. Le applicazioni di Flash di Adobe possono richiedere l'accesso alle proprietà delle immagini fornite con fmt=swf o fmt=swf3.
seo-title: TrustedDomains
solution: Experience Manager
title: TrustedDomains
uuid: 1d056d68-b699-413c-897c-8612444735c5
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

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
