---
title: Utilizzo di mappe di illuminazione multipla
description: Alcune applicazioni possono richiedere una mappa di illuminazione diversa per diversi tipi di materiali.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Utilizzo di mappe di illuminazione multipla{#using-multiple-illumination-maps}

Alcune applicazioni possono richiedere una mappa di illuminazione diversa per diversi tipi di materiali.

È possibile creare fino a tre mappe di illuminazione per ogni vignetta. La mappa di illuminazione per un&#39;operazione di rendering viene selezionata con la `illum=` e `gloss=` comandi.

**Selezione predefinita** - Se `illum=` o `gloss=` non sono specificati, il renderer utilizza la prima mappa di illuminazione creata (in genere mappa A, alias mappa di illuminazione &quot;Flat&quot;).

**Selezione automatica con`gloss=`** - Se `illum=` non è specificato o è impostato su `-1`, il renderer confronta il `gloss=` valore con i valori di brillantezza associati a ogni mappa di illuminazione nella vignetta. Sceglie la mappa di illuminazione il cui valore di brillantezza è più vicino al valore specificato `gloss=`.

**Selezione esplicita con`illum=`** - Se `illum=` è specificato e impostato su `0`, `1`oppure `2`, il renderer utilizza la corrispondente mappa di illuminazione; `gloss=` viene ignorato per la selezione della mappa di illuminazione.

Se la vignetta contiene una sola mappa di illuminazione, il renderer utilizza tale mappa e ignora il `illum=` e `gloss=` comandi.
