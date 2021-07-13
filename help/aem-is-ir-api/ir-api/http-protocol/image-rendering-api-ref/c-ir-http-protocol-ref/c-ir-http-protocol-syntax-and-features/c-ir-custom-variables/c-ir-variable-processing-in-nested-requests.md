---
description: I riferimenti $var$ possono verificarsi ovunque all'interno delle parentesi graffe di una richiesta Image Server o Image Rendering nidificata, inclusa a sinistra del '?' separazione del percorso dalla query.
solution: Experience Manager
title: Elaborazione delle variabili nelle richieste nidificate
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# Elaborazione delle variabili nelle richieste nidificate{#variable-processing-in-nested-requests}

I riferimenti $var$ possono verificarsi ovunque all&#39;interno delle parentesi graffe di una richiesta Image Server o Image Rendering nidificata, inclusa a sinistra del &#39;?&#39; separazione del percorso dalla query.

Il server sostituisce questi riferimenti con i valori (dall’url o da `catalog::Modifier` del catalogo immagini principale) prima di analizzare ed elaborare ulteriormente la richiesta nidificata.

Inoltre, tutte le definizioni `$ *[!DNL var]*=` dell’url e `catalog::Modifier` vengono inoltrate a tutte le richieste nidificate di Image Server e Image Rendering. In questo modo tutte le definizioni di variabili sono disponibili per tutti i modelli, indipendentemente dal livello di nidificazione.

Indipendentemente dal livello di nidificazione, solo la codifica HTTP a passo singolo deve essere applicata ai valori delle variabili che devono essere sostituiti in qualsiasi punto delle richieste Image Rendering nidificate o Image Serving.
