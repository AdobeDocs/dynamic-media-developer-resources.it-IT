---
description: Generato quando un utente autenticato non dispone di autorizzazioni sufficienti per eseguire un'attività.
solution: Experience Manager
title: authorizationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 22%

---


# authorizationFault{#authorizationfault}

Generato quando un utente autenticato non dispone di autorizzazioni sufficienti per eseguire un&#39;attività.

Sintassi

## Tipi di errore {#section-1f04dec489714ee6bb7256fae6ab7730}

| ID | Guasto |
|---|---|
| 20000 | `AUTHORIZATION_FAULT_CODE_INVALID_COMPANY` |
| 20001 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USERNAME` |
| 2002 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USER` |
| 2003 | `AUTHORIZATION_FAULT_CODE_NO_OPERATION_PERMISSION` |
| 2004 | `AUTHORIZATION_FAULT_CODE_NO_IMPERSONATION_PERMISSION` |
| 2005 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_PARAMETER_VALUE` |
| 2006 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_COMPANY` |
| 2007 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_REQUEST_USER` |
| 2008 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_ACCESS_GROUP` |
| 2009 | `AUTHORIZATION_FAULT_CODE_MISSING_PERMISSION` |

## Campi di errore {#section-4e3e41f41fea402a9ae314bfd05f663e}

| Nome | Tipo | Descrizione |
|---|---|---|
| `code` | `xsd:int` | ID errore |
| `reason` | `xsd:string` | Messaggio informativo che descrive l&#39;errore. |

