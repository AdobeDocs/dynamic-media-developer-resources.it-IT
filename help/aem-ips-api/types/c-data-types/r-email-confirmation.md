---
description: Invia un'e-mail a un destinatario designato in risposta a un'operazione cdnCacheInvalidation.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 4%

---


# EmailConfirmation{#emailconfirmation}

Invia un&#39;e-mail a un destinatario designato in risposta a un&#39;operazione cdnCacheInvalidation.

Sintassi

## Parametri {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Se true, include l’account utente del servizio Web dell’utente, che è un elenco di e-mail designate per ricevere una conferma e-mail dalla rete CDN di Dynamic Media. |
| `*`ccOthersArray`*` | `types:EmailArray` | Array di indirizzi e-mail (massimo 5) designati per ricevere la notifica di conferma dal CDN di Dynamic Media. |

