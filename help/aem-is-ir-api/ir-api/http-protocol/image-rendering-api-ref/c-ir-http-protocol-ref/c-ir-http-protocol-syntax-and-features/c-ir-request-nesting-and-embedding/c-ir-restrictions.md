---
description: Alcune limitazioni si applicano alla nidificazione e all’incorporazione.
seo-description: Alcune limitazioni si applicano alla nidificazione e all’incorporazione.
seo-title: Restrizioni
solution: Experience Manager
title: Restrizioni
topic: Scene7 Image Serving - Image Rendering API
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# Limitazioni{#restrictions}

Alcune limitazioni si applicano alla nidificazione e all’incorporazione.

Per una buona prestazione del server, la risoluzione delle immagini restituite dalle richieste nidificate deve corrispondere ragionevolmente alla risoluzione della texture degli oggetti a cui viene applicato il materiale.

Le immagini straniere vengono memorizzate nella cache locale. Eventuali modifiche apportate a tali immagini verranno rilevate solo dopo che la voce della cache locale diventerà obsoleta (in base all&#39;intestazione HTTP scaduta).
