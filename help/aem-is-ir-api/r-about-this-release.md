---
description: Image Serving 6.6.1 e Image Rendering 6.6.1 sostituiscono Image Serving 6.5.3 e Image Rendering 6.5.3.
solution: Experience Manager
title: Informazioni su questa versione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
TQID: 'https://experienceleague.adobe.com/Mv84kHB7jsBYAvY1j--l8Ly5VZtKwFq-SsNdz2TIQOE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 0%

---

# Informazioni su questa versione{#about-this-release}

Image Serving 6.6.1 e Image Rendering 6.6.1 sostituiscono Image Serving 6.5.3 e Image Rendering 6.5.3.

## Problemi noti e modifiche del comportamento {#section-9dbc05206187477f926a78e8108a34e1}

* L’utilizzo del carattere del punto interrogativo negli ID risorsa non è più supportato, anche se il carattere è codificato in URL.
* Le richieste del banner dinamico `/xfl/flash/` non sono più supportate e ora restituiscono un codice di errore HTTP 404.
* Le richieste W2P `/is/agm/` non sono più supportate.
* Alcuni messaggi di errore non vengono più visualizzati nel browser. Per eseguire il debug, è quindi necessario rivedere il registro di traccia.

## Nuove funzioni {#section-b1386e36cb4544ebb79766a06b16842d}

* Campione avanzato
* Ritaglio avanzato

## Correzione bug {#section-58dff74d56f64edeadf8f8b97b7a4161}

* È stato risolto un problema a causa del quale l&#39;opzione RTF `\qc` seguita da uno spazio impediva il rendering di una richiesta.
