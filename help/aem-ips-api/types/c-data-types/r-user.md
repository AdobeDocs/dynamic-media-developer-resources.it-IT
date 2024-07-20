---
description: Utente di risorse e tipi nel sistema.
solution: Experience Manager
title: Utente
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 5%

---

# [!DNL User]{#user}

Utente di risorse e tipi nel sistema.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| userHandle | `xsd:string` | Handle utente. |
| firstName | `xsd:string` | Nome utente. |
| lastName | `xsd:string` | Cognome utente. |
| email | `xsd:string` | indirizzo e-mail. |
| defaultRole | `xsd:string` | Imposta il ruolo di un utente in ogni società a cui appartiene. Tuttavia, il ruolo utente `IpsAmin` sostituisce gli altri ruoli utente. |
| isValid | `xsd:boolean` | Determina se l&#39;utente è valido. |
| passwordExpires | `xsd:dateTime` | Imposta la data di scadenza della password. |
