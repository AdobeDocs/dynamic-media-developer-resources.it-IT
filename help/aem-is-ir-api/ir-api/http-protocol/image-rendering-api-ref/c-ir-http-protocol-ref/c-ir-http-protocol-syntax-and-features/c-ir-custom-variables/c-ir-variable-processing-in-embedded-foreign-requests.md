---
description: I riferimenti $var$ che si verificano in qualsiasi punto all'interno delle parentesi graffe di una richiesta esterna incorporata sono sostituiti dai valori di definizione della variabile corrispondenti.
solution: Experience Manager
title: Elaborazione variabile nelle richieste esterne incorporate
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# Elaborazione delle variabili nelle richieste esterne incorporate{#variable-processing-in-embedded-foreign-requests}

I riferimenti $var$ che si verificano in qualsiasi punto all&#39;interno delle parentesi graffe di una richiesta esterna incorporata sono sostituiti dai valori di definizione della variabile corrispondenti.

Questo consente di inserire richieste esterne incorporate in un modello in un catalogo immagini.

I valori delle variabili che devono essere sostituiti in richieste esterne in genere devono essere codificati in doppia codifica, poiché non viene applicata alcuna nuova codifica prima che il server tenti di trasmettere l’URL esterno finale.
