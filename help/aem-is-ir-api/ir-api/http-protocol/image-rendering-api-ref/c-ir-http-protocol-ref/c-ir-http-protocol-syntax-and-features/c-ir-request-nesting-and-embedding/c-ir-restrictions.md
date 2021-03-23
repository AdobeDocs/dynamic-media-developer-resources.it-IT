---
description: Alcune restrizioni si applicano alla nidificazione e all’incorporazione.
seo-description: Alcune restrizioni si applicano alla nidificazione e all’incorporazione.
seo-title: Restrizioni
solution: Experience Manager
title: Restrizioni
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# Restrizioni{#restrictions}

Alcune restrizioni si applicano alla nidificazione e all’incorporazione.

Per buone prestazioni del server, la risoluzione delle immagini restituite dalle richieste nidificate deve corrispondere ragionevolmente alla risoluzione della texture degli oggetti a cui viene applicato il materiale.

Le immagini esterne vengono memorizzate nella cache locale. Eventuali modifiche a tali immagini verranno rilevate solo dopo che la voce della cache locale diventa obsoleta (in base all’intestazione HTTP scadente).
