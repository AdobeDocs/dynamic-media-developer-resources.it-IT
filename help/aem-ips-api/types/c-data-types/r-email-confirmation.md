---
description: Invia un'e-mail a un destinatario designato in risposta a un'operazione cdnCacheInvalidation.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# EmailConfirmation{#emailconfirmation}

Invia un&#39;e-mail a un destinatario designato in risposta a un&#39;operazione cdnCacheInvalidation.

Sintassi

## Parametri {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nome | Tipo | Descrizione |
|---|---|---|
| ccOriginator | `xsd:boolean` | Se true, include l’account utente del servizio Web dell’utente, che è un elenco di e-mail designate per ricevere una conferma e-mail dalla rete CDN di Dynamic Media. |
| ccOthersArray | `types:EmailArray` | Array di indirizzi e-mail (massimo 5) designati per ricevere la notifica di conferma dal CDN di Dynamic Media. |
