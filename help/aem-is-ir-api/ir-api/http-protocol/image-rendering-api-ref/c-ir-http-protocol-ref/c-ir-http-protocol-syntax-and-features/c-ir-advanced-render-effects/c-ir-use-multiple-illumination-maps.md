---
description: Alcune applicazioni possono richiedere una diversa mappa di illuminazione per diversi tipi di materiali.
seo-description: Alcune applicazioni possono richiedere una diversa mappa di illuminazione per diversi tipi di materiali.
seo-title: Utilizzo di più mappe di illuminazione
solution: Experience Manager
title: Utilizzo di più mappe di illuminazione
topic: Scene7 Image Serving - Image Rendering API
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# Utilizzo di più mappe di illuminazione{#using-multiple-illumination-maps}

Alcune applicazioni possono richiedere una diversa mappa di illuminazione per diversi tipi di materiali.

Per ogni vignettatura è possibile creare fino a tre mappe di illuminazione. La mappa di illuminazione per un&#39;operazione di rendering viene selezionata con i comandi `illum=` e `gloss=`.

**** Selezione predefinitaSe non viene specificato  `illum=` né  `gloss=` viene specificato alcun valore, il renderer utilizzerà la prima mappa di illuminazione creata (in genere mappa A, detta mappa di illuminazione piatta).

**Selezione automatica con`gloss=`** Se non  `illum=` è specificato o è impostato su -1, il renderer confronta il  `gloss=` valore specificato con i valori globali associati a ciascuna mappa di illuminazione nella vignettatura e sceglie la mappa di illuminazione il cui valore globale è più vicino a quello specificato  `gloss=`.

**Selezione esplicita con`illum=`** Se  `illum=` è specificato e impostato su 0, 1 o 2, il renderer utilizzerà la mappa di illuminazione corrispondente;  `gloss=` viene ignorato allo scopo di selezionare la mappa di illuminazione.

Se la vignettatura contiene una sola mappa di illuminazione, il renderer utilizzerà tale mappa e ignorerà i comandi `illum=` e `gloss=`.
