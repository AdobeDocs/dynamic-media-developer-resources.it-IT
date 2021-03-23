---
description: Il passaggio 2 delle trasformazioni del livello immagine viene modificato come segue per le miniature (ad esempio, se req=tmb).
seo-description: Il passaggio 2 delle trasformazioni del livello immagine viene modificato come segue per le miniature (ad esempio, se req=tmb).
seo-title: Ridimensionamento delle miniature
solution: Experience Manager
title: Ridimensionamento delle miniature
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Ridimensionamento delle miniature{#thumbnail-scaling}

Il passaggio 2 delle trasformazioni del livello immagine viene modificato come segue per le miniature (ad esempio, se req=tmb).

* `2.` Se  `size=` è specificato, inserisci l’immagine (ritagliata) nel  `size=` corretto utilizzando le regole delle miniature. Se `size=` non è specificato, ridimensiona in base a `res=` oppure, se `res=` non è specificato, inserisci l’immagine (ritagliata) nel campo canvas utilizzando le regole di miniatura descritte di seguito.

