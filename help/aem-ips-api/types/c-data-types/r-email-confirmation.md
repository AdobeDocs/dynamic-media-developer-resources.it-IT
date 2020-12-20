---
description: Invia un'e-mail a un destinatario designato in risposta a un'operazione cdnCacheInvalidation.
seo-description: Invia un'e-mail a un destinatario designato in risposta a un'operazione cdnCacheInvalidation.
seo-title: EmailConfirm
solution: Experience Manager
title: EmailConfirm
topic: Scene7 Image Production System API
uuid: c3b7aada-a03a-418d-80b2-31a86a1af786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 4%

---


# EmailConfirm{#emailconfirmation}

Invia un&#39;e-mail a un destinatario designato in risposta a un&#39;operazione cdnCacheInvalidation.

Sintassi

## Parametri {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`ccOriginator`*` | `xsd:boolean` | Se true, include l&#39;account utente del servizio Web dell&#39;utente, che è un elenco di e-mail designate per ricevere una conferma e-mail dalla rete CDN di Scene7. |
| ` *`ccOthersArray`*` | `types:EmailArray` | Un array di indirizzi e-mail (massimo 5) destinati a ricevere la notifica di conferma dalla rete CDN Scene7. |

