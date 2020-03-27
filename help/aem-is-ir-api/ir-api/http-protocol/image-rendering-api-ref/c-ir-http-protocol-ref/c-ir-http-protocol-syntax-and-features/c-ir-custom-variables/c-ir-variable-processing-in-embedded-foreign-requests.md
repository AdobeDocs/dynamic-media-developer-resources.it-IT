---
description: I riferimenti $var$ che si verificano ovunque all'interno delle parentesi graffe di una richiesta esterna incorporata vengono sostituiti con valori di definizione variabili corrispondenti.
seo-description: I riferimenti $var$ che si verificano ovunque all'interno delle parentesi graffe di una richiesta esterna incorporata vengono sostituiti con valori di definizione variabili corrispondenti.
seo-title: Elaborazione delle variabili nelle richieste esterne incorporate
solution: Experience Manager
title: Elaborazione delle variabili nelle richieste esterne incorporate
topic: Scene7 Image Serving - Image Rendering API
uuid: b4334a2e-dab1-4458-ab3d-bb79d2c4fdd4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Elaborazione delle variabili nelle richieste esterne incorporate{#variable-processing-in-embedded-foreign-requests}

I riferimenti $var$ che si verificano ovunque all&#39;interno delle parentesi graffe di una richiesta esterna incorporata vengono sostituiti con valori di definizione variabili corrispondenti.

Questo consente di inserire richieste esterne incorporate in un modello in un catalogo immagini.

I valori delle variabili che devono essere sostituiti in richieste esterne in genere devono essere codificati due volte, poiché non viene applicata alcuna codifica prima che il server tenti di trasmettere l&#39;URL esterno finale.
