---
description: Il passaggio 2 delle trasformazioni del livello dell’immagine viene modificato come segue per le miniature (ad es. se req=tmb).
seo-description: Il passaggio 2 delle trasformazioni del livello dell’immagine viene modificato come segue per le miniature (ad es. se req=tmb).
seo-title: Ridimensionamento delle miniature
solution: Experience Manager
title: Ridimensionamento delle miniature
topic: Scene7 Image Serving - Image Rendering API
uuid: df935d40-84c6-4018-9e41-faef4653ff1f
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# Ridimensionamento delle miniature{#thumbnail-scaling}

Il passaggio 2 delle trasformazioni del livello dell’immagine viene modificato come segue per le miniature (ad es. se req=tmb).

* `2.` Se  `size=` è specificato, inserite l’immagine (ritagliata) nel  `size=` rect utilizzando le regole delle miniature. Se `size=` non è specificato, ridimensionate in base a `res=` oppure, se `res=` non è specificato, inserite l&#39;immagine (ritagliata) nel quadro rect utilizzando le regole di miniatura descritte di seguito.

