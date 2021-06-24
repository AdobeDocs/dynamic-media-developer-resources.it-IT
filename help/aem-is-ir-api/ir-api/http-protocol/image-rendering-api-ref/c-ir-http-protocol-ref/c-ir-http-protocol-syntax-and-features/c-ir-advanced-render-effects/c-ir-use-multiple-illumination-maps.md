---
description: Alcune applicazioni possono richiedere una mappa di illuminazione diversa per diversi tipi di materiali.
solution: Experience Manager
title: Utilizzo di mappe di illuminazione multipla
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Utilizzo di mappe di illuminazione multipla{#using-multiple-illumination-maps}

Alcune applicazioni possono richiedere una mappa di illuminazione diversa per diversi tipi di materiali.

È possibile creare fino a tre mappe di illuminazione per ogni vignetta. La mappa di illuminazione per un&#39;operazione di rendering viene selezionata con i comandi `illum=` e o `gloss=`.

**Selezione** predefinitaSe non  `illum=` vengono specificati né  `gloss=` né il modulo di rendering, il modulo di rendering utilizzerà la prima mappa di illuminazione creata (in genere mappa A, ovvero la mappa di illuminazione &quot;Flat&quot;).

**Selezione automatica con`gloss=`** Se non  `illum=` è specificato o è impostato su -1, il renderer confronta il  `gloss=` valore specificato con i valori della lucentezza associati a ogni mappa di illuminazione nella vignetta e scegli la mappa di illuminazione il cui valore della lucentezza è più vicino al valore specificato  `gloss=`.

**Selezione esplicita con`illum=`** Se  `illum=` è specificato e impostato su 0, 1 o 2, il renderer utilizzerà la mappa di illuminazione corrispondente;  `gloss=` viene ignorato allo scopo di selezionare la mappa di illuminazione.

Se la vignetta contiene una sola mappa di illuminazione, il modulo di rendering la utilizzerà e ignorerà i comandi `illum=` e `gloss=`.
