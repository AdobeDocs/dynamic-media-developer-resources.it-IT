---
description: Invia un messaggio e-mail a un destinatario designato in risposta a un'operazione cdnCacheInvalidation.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 3%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

Invia un messaggio e-mail a un destinatario designato in risposta a un&#39;operazione cdnCacheInvalidation.

Sintassi

## Parametri {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nome | Tipo | Descrizione |
|---|---|---|
| ccOriginator | `xsd:boolean` | Se true, include l’account utente del servizio web dell’utente, che è un elenco di e-mail designate per ricevere una conferma e-mail dalla rete CDN di Dynamic Medie. |
| ccOthersArray | `types:EmailArray` | Un array di indirizzi e-mail (massimo 5) designati per ricevere la notifica di conferma dal CDN di Dynamic Medie. |
