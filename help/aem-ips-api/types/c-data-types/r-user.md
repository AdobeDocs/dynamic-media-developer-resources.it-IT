---
description: Utente di risorse e tipi nel sistema.
solution: Experience Manager
title: Utente
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 9%

---

# Utente{#user}

Utente di risorse e tipi nel sistema.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`userHandle`*` | `xsd:string` | Maniglia utente. |
| `*`firstName`*` | `xsd:string` | Nome utente. |
| `*`lastName`*` | `xsd:string` | Cognome utente. |
| `*`e-mail`*` | `xsd:string` | indirizzo e-mail. |
| `*`defaultRole`*` | `xsd:string` | Imposta il ruolo di un utente in ogni società a cui appartiene. Tuttavia, il ruolo utente `IpsAmin` esclude altri ruoli utente. |
| `*`isValid`*` | `xsd:boolean` | Determina se l&#39;utente è valido. |
| `*`passwordExpires`*` | `xsd:dateTime` | Imposta la data di scadenza della password. |
