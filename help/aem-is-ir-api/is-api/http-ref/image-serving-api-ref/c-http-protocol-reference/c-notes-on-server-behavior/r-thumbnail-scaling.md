---
description: Il passaggio 2 delle trasformazioni del livello immagine viene modificato come segue per le miniature (ad esempio, se req=tmb).
solution: Experience Manager
title: Ridimensionamento delle miniature
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Ridimensionamento delle miniature{#thumbnail-scaling}

Il passaggio 2 delle trasformazioni del livello immagine viene modificato come segue per le miniature (ad esempio, se req=tmb).

* `2.` Se  `size=` è specificato, inserisci l’immagine (ritagliata) nel  `size=` corretto utilizzando le regole delle miniature. Se `size=` non è specificato, ridimensiona in base a `res=` oppure, se `res=` non è specificato, inserisci l’immagine (ritagliata) nel campo canvas utilizzando le regole di miniatura descritte di seguito.
