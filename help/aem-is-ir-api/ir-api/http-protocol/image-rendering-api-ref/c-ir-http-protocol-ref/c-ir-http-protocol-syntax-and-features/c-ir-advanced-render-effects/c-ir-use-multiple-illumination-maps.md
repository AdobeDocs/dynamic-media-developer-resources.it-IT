---
title: Utilizzo di mappe di illuminazione multipla
description: Alcune applicazioni possono richiedere una mappa di illuminazione diversa per diversi tipi di materiali.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
TQID: 'https://experienceleague.adobe.com/VVZ1IdVJ85V-mIrdN6O8Vs-gb4PTsnjxyHnC8oEh1y0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 166
ht-degree: 0%

---

# Utilizzo di mappe di illuminazione multipla{#using-multiple-illumination-maps}

Alcune applicazioni possono richiedere una mappa di illuminazione diversa per diversi tipi di materiali.

Per ogni vignettatura è possibile creare fino a tre mappe di illuminazione. La mappa di illuminazione per un&#39;operazione di rendering è selezionata con i comandi `illum=` e/o `gloss=`.

**Selezione predefinita** - Se `illum=` o `gloss=` non sono specificati, il renderer utilizza la prima mappa di illuminazione creata (in genere la mappa A, ovvero la mappa di illuminazione &#39;Piatta&#39;).

**Selezione automatica con`gloss=`** - Se `illum=` non è specificato o è impostato su `-1`, il renderer confronta il valore `gloss=` specificato con i valori di lucentezza associati a ogni mappa di illuminazione nella vignettatura. Scegli la mappa di illuminazione il cui valore di lucentezza è più vicino al `gloss=` specificato.

**Selezione esplicita con`illum=`** - Se `illum=` è specificato e impostato su `0`, `1` o `2`, il renderer utilizza la mappa di illuminazione corrispondente; `gloss=` viene ignorato per la selezione della mappa di illuminazione.

Se la vignettatura contiene una sola mappa di illuminazione, il renderer utilizza tale mappa e ignora i comandi `illum=` e `gloss=`.
