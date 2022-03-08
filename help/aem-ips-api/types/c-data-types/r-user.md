---
description: Utente di risorse e tipi nel sistema.
solution: Experience Manager
title: Utente
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 9%

---

# Utente{#user}

Utente di risorse e tipi nel sistema.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| userHandle | `xsd:string` | Maniglia utente. |
| firstName | `xsd:string` | Nome utente. |
| lastName | `xsd:string` | Cognome utente. |
| e-mail | `xsd:string` | indirizzo e-mail. |
| defaultRole | `xsd:string` | Imposta il ruolo di un utente in ogni società a cui appartiene. Tuttavia, il ruolo utente `IpsAmin` sostituisce altri ruoli utente. |
| isValid | `xsd:boolean` | Determina se l&#39;utente è valido. |
| passwordExpires | `xsd:dateTime` | Imposta la data di scadenza della password. |
