---
description: Oltre al dimensionamento (size=) e al posizionamento (pos=) dei livelli relativi al livello 0 e alla specifica dell'ordine di composizione (l'ordine z) con il comando layer=, i livelli possono essere ruotati (rotate=) e capovolti (flip=).
solution: Experience Manager
title: Operazioni a livello
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# Operazioni a livello{#layer-operations}

Oltre al dimensionamento (size=) e al posizionamento (pos=) dei livelli relativi al livello 0 e alla specifica dell&#39;ordine di composizione (l&#39;ordine z) con il comando layer=, i livelli possono essere ruotati (rotate=) e capovolti (flip=).

Gli attributi `origin=` e `anchor=` possono essere utilizzati per mantenere l’allineamento desiderato tra i livelli quando le immagini o il testo vengono modificati dinamicamente nei modelli.

Il comando `maskUse=` è disponibile per i livelli immagine per accedere all&#39;area di sfondo delle immagini che hanno maschere separate.

`opac=` può essere utilizzato per variare l&#39;opacità del livello e  `hide=` per mostrare o nascondere il livello.
