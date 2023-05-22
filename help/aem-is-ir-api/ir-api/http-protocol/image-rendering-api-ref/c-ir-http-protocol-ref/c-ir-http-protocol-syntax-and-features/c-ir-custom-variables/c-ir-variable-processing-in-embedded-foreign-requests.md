---
title: Elaborazione delle variabili nelle richieste esterne incorporate
description: I riferimenti $var$ che si verificano in qualsiasi punto all'interno delle parentesi graffe di una richiesta esterna incorporata vengono sostituiti con valori di definizione della variabile corrispondenti.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Elaborazione delle variabili nelle richieste esterne incorporate{#variable-processing-in-embedded-foreign-requests}

Qualsiasi `$var$` i riferimenti che si verificano in qualsiasi punto all’interno delle parentesi graffe di una richiesta esterna incorporata vengono sostituiti con valori di definizione delle variabili corrispondenti.

Consente di inserire richieste esterne incorporate in un modello in un catalogo immagini.

I valori delle variabili che devono essere sostituiti in richieste esterne in genere devono avere una doppia codifica, perché non viene applicata alcuna nuova codifica prima che il server tenti di trasmettere l’URL esterno finale.
