---
description: Il passaggio 2 delle trasformazioni del livello immagine viene modificato come segue per le miniature (ad esempio, se req=tmb).
solution: Experience Manager
title: Ridimensionamento delle miniature
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Ridimensionamento delle miniature{#thumbnail-scaling}

Il passaggio 2 delle trasformazioni del livello immagine viene modificato come segue per le miniature (ad esempio, se req=tmb).

* `2.` Se  `size=` è specificato, inserisci l’immagine (ritagliata) nel  `size=` corretto utilizzando le regole delle miniature. Se `size=` non è specificato, ridimensiona in base a `res=` oppure, se `res=` non è specificato, inserisci l’immagine (ritagliata) nel campo canvas utilizzando le regole di miniatura descritte di seguito.

