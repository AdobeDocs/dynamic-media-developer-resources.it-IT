---
description: I riferimenti $var$ possono verificarsi ovunque all'interno delle parentesi graffe di una richiesta Image Server o Image Rendering nidificata, inclusa a sinistra del '?' separazione del percorso dalla query.
seo-description: I riferimenti $var$ possono verificarsi ovunque all'interno delle parentesi graffe di una richiesta Image Server o Image Rendering nidificata, inclusa a sinistra del '?' separazione del percorso dalla query.
seo-title: Elaborazione delle variabili nelle richieste nidificate
solution: Experience Manager
title: Elaborazione delle variabili nelle richieste nidificate
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# Elaborazione delle variabili nelle richieste nidificate{#variable-processing-in-nested-requests}

I riferimenti $var$ possono verificarsi ovunque all&#39;interno delle parentesi graffe di una richiesta Image Server o Image Rendering nidificata, inclusa a sinistra del &#39;?&#39; separazione del percorso dalla query.

Il server sostituisce questi riferimenti con i valori (dall’url o da `catalog::Modifier` del catalogo immagini principale) prima di analizzare ed elaborare ulteriormente la richiesta nidificata.

Inoltre, tutte le definizioni `$ *[!DNL var]*=` dell’url e `catalog::Modifier` vengono inoltrate a tutte le richieste nidificate di Image Server e Image Rendering. In questo modo tutte le definizioni di variabili sono disponibili per tutti i modelli, indipendentemente dal livello di nidificazione.

Indipendentemente dal livello di nidificazione, solo la codifica HTTP a passo singolo deve essere applicata ai valori delle variabili che devono essere sostituiti in qualsiasi punto delle richieste Image Rendering nidificate o Image Serving.
