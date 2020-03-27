---
description: $var$ i riferimenti possono verificarsi ovunque all'interno delle parentesi graffe di una richiesta nidificata di Image Serving o Image Rendering, inclusa la parte sinistra dell'?' separazione del percorso dalla query.
seo-description: $var$ i riferimenti possono verificarsi ovunque all'interno delle parentesi graffe di una richiesta nidificata di Image Serving o Image Rendering, inclusa la parte sinistra dell'?' separazione del percorso dalla query.
seo-title: Elaborazione delle variabili nelle richieste nidificate
solution: Experience Manager
title: Elaborazione delle variabili nelle richieste nidificate
topic: Scene7 Image Serving - Image Rendering API
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Elaborazione delle variabili nelle richieste nidificate{#variable-processing-in-nested-requests}

$var$ i riferimenti possono verificarsi ovunque all&#39;interno delle parentesi graffe di una richiesta nidificata di Image Serving o Image Rendering, inclusa la parte sinistra dell&#39;?&#39; separazione del percorso dalla query.

Il server sostituisce questi riferimenti con valori (dall’URL o dal catalogo immagini principale) prima `catalog::Modifier` di analizzare ed elaborare ulteriormente la richiesta nidificata.

Inoltre, tutte `$ *[!DNL var]*=` le definizioni dell’URL e `catalog::Modifier` vengono inoltrate a tutte le richieste nidificate di Image Server e di rendering delle immagini. In questo modo tutte le definizioni delle variabili sono disponibili per tutti i modelli, indipendentemente dal livello di nidificazione.

Indipendentemente dal livello di nidificazione, ai valori variabili che devono essere sostituiti in qualsiasi punto delle richieste nidificate di rendering di immagini o di Image Server deve essere applicata solo la codifica HTTP a passata singola.
