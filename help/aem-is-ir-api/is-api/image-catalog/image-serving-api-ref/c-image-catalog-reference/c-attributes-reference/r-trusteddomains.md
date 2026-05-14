---
description: Domini web delle applicazioni Flash. Le applicazioni Adobe Flash possono richiedere l'accesso alle proprietà delle immagini fornite con fmt=swf o fmt=swf3.
solution: Experience Manager
title: Domini attendibili
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
TQID: 'https://experienceleague.adobe.com/xGn-usdBOB3NjRaffq6w0SJDlDerpeQJHGhKej-L3Cw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 2%

---

# Domini attendibili{#trusteddomains}

Domini web delle applicazioni Flash. Le applicazioni Adobe Flash possono richiedere l&#39;accesso alle proprietà delle immagini fornite con fmt=swf o fmt=swf3.

Il file SWF deve concedere esplicitamente l&#39;accesso registrando il nome dei domini dell&#39;applicazione considerati attendibili.

## Proprietà {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Stringa contenente un elenco separato da virgole di nomi di dominio web. Se vuoto, le applicazioni devono essere servite dallo stesso dominio di Image Rendering per poter accedere alle proprietà delle immagini nelle risposte in formato SWF.

## Predefinito {#section-5c52ed3c7310488380f5a6f9540bf981}

Ereditato da `default::TrustedDomains` se non presente.

## Consultate anche {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
