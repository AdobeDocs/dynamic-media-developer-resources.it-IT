---
description: Domini Web dell’applicazione Flash. Le applicazioni Adobe Flash possono richiedere l'accesso alle proprietà delle immagini fornite con fmt=swf o fmt=swf3.
seo-description: Domini Web dell’applicazione Flash. Le applicazioni Adobe Flash possono richiedere l'accesso alle proprietà delle immagini fornite con fmt=swf o fmt=swf3.
seo-title: TrustedDomains
solution: Experience Manager
title: TrustedDomains
topic: Scene7 Image Serving - Image Rendering API
uuid: 1d056d68-b699-413c-897c-8612444735c5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TrustedDomains{#trusteddomains}

Domini Web dell’applicazione Flash. Le applicazioni Adobe Flash possono richiedere l&#39;accesso alle proprietà delle immagini fornite con fmt=swf o fmt=swf3.

Il file swf deve concedere l’accesso esplicitamente registrando il nome dei domini applicazione di cui si fida.

## Proprietà {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Stringa contenente un elenco separato da virgole di nomi di dominio Web. Se vuoto, le applicazioni devono essere servite dallo stesso dominio del rendering delle immagini per poter accedere alle proprietà delle immagini nelle risposte in formato swf.

## Predefinito {#section-5c52ed3c7310488380f5a6f9540bf981}

Ereditato da `default::TrustedDomains` se non presente.

## Consultate anche {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
