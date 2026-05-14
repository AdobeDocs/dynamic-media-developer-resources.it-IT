---
description: Utente di risorse e tipi nel sistema.
solution: Experience Manager
title: Utente
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
TQID: 'https://experienceleague.adobe.com/XM-2FjVie-j71W3Sc3-TypNJUFnz5AQuZZuGOx1fePs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
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
