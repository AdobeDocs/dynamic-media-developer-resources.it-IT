---
description: Un utente di risorse e tipi nel sistema.
seo-description: Un utente di risorse e tipi nel sistema.
seo-title: Utente
solution: Experience Manager
title: Utente
topic: Dynamic Media Image Production System API
uuid: 37e939ae-dd1a-4550-aa93-b7b091ebc339
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 9%

---


# Utente{#user}

Un utente di risorse e tipi nel sistema.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`userHandle`*` | `xsd:string` | handle utente. |
| `*`firstName`*` | `xsd:string` | Nome utente. |
| `*`lastName`*` | `xsd:string` | Cognome utente. |
| `*`e-mail`*` | `xsd:string` | indirizzo e-mail. |
| `*`defaultRole`*` | `xsd:string` | Imposta il ruolo per un utente in ogni società a cui appartiene. Tuttavia, il ruolo utente `IpsAmin` ha la priorità su altri ruoli utente. |
| `*`isInvalid`*` | `xsd:boolean` | Determina se l&#39;utente è valido. |
| `*`passwordExpires`*` | `xsd:dateTime` | Imposta la data di scadenza della password. |

