---
title: Ridimensionamento miniature
description: Il passaggio 2 del livello immagine viene modificato come segue per le miniature (ovvero, se req=tmb).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# Ridimensionamento miniature{#thumbnail-scaling}

Il passaggio 2 del livello immagine viene modificato come segue per le miniature (ovvero, se req=tmb).

* `2.` Se si specifica `size=`, adattare l&#39;immagine (ritagliata) al retto `size=` utilizzando le regole per le miniature. Se `size=` non è specificato, ridimensionare in base a `res=` oppure, se `res=` non è specificato, adattare l&#39;immagine (ritagliata) all&#39;area di lavoro utilizzando le regole di miniatura descritte di seguito.
