---
description: Generato quando un utente non può essere autenticato.
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 15%

---


# authenticationFault{#authenticationfault}

Generato quando un utente non può essere autenticato.

Sintassi

## Tipi di errore {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | Guasto |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## Campi di errore {#section-1fe84846a7154b03ab49552810ee9ac3}

| Nome | Tipo | Descrizione |
|---|---|---|
| `code` | `xsd:int` | ID errore |
| `reason` | `xsd:string` | Messaggio informativo che descrive l&#39;errore. |
