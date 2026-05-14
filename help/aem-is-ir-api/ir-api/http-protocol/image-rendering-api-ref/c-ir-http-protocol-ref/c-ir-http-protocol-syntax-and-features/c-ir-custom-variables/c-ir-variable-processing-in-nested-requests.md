---
title: Elaborazione delle variabili nelle richieste nidificate
description: I riferimenti $var$ possono verificarsi ovunque all’interno delle parentesi graffe di una richiesta di Image Server o Image Rendering nidificata, incluso a sinistra del carattere "?" che separa il percorso dalla query.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
TQID: 'https://experienceleague.adobe.com/m7BlSGU8gSozgp8fvNcWuMz5uvpUrfMi4fV5yCYH5bs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 0%

---

# Elaborazione delle variabili nelle richieste nidificate{#variable-processing-in-nested-requests}

I riferimenti $var$ possono verificarsi ovunque all’interno delle parentesi graffe di una richiesta di Image Server o Image Rendering nidificata, incluso a sinistra del carattere &quot;?&quot; che separa il percorso dalla query.

Il server sostituisce questi riferimenti con valori (provenienti dall&#39;URL o da `catalog::Modifier` del catalogo principale delle immagini) prima di analizzare ed elaborare ulteriormente la richiesta nidificata.

Inoltre, tutte le definizioni di `$ *[!DNL var]*=` dall&#39;URL e `catalog::Modifier` vengono inoltrate a tutte le richieste nidificate di Image Server e Image Rendering. In questo modo tutte le definizioni di variabili saranno disponibili per tutti i modelli, indipendentemente dal livello di nidificazione.

Indipendentemente dal livello di nidificazione, solo la codifica HTTP a passata singola deve essere applicata ai valori delle variabili che devono essere sostituiti ovunque nelle richieste di Image Rendering o Image Server nidificate.
