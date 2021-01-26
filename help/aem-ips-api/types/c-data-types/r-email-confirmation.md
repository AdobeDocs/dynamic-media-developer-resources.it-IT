---
description: Invia un'e-mail a un destinatario designato in risposta a un'operazione cdnCacheInvalidation.
solution: Experience Manager
title: EmailConfirm
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---


# EmailConfirm{#emailconfirmation}

Invia un&#39;e-mail a un destinatario designato in risposta a un&#39;operazione cdnCacheInvalidation.

Sintassi

## Parametri {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Se true, include l&#39;account utente del servizio Web dell&#39;utente, che è un elenco di e-mail designate per ricevere una conferma e-mail dalla rete CDN di Dynamic Media. |
| `*`ccOthersArray`*` | `types:EmailArray` | Un array di indirizzi e-mail (massimo 5) destinati a ricevere la notifica di conferma dalla rete CDN Dynamic Media. |

