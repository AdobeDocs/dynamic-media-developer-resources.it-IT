---
description: I riferimenti $var$ che si verificano in qualsiasi punto all'interno delle parentesi graffe di una richiesta esterna incorporata sono sostituiti dai valori di definizione della variabile corrispondenti.
solution: Experience Manager
title: Elaborazione variabile nelle richieste esterne incorporate
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Elaborazione variabile nelle richieste esterne incorporate{#variable-processing-in-embedded-foreign-requests}

I riferimenti $var$ che si verificano in qualsiasi punto all&#39;interno delle parentesi graffe di una richiesta esterna incorporata sono sostituiti dai valori di definizione della variabile corrispondenti.

Questo consente di inserire richieste esterne incorporate in un modello in un catalogo immagini.

I valori delle variabili che devono essere sostituiti in richieste esterne in genere devono essere codificati in doppia codifica, poiché non viene applicata alcuna nuova codifica prima che il server tenti di trasmettere l’URL esterno finale.
