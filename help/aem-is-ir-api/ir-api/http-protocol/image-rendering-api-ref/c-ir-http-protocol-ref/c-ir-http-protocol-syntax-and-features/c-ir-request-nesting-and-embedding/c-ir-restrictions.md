---
description: Alcune restrizioni si applicano alla nidificazione e all’incorporazione.
solution: Experience Manager
title: Restrizioni
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# Restrizioni{#restrictions}

Alcune restrizioni si applicano alla nidificazione e all’incorporazione.

Per buone prestazioni del server, la risoluzione delle immagini restituite dalle richieste nidificate deve corrispondere ragionevolmente alla risoluzione della texture degli oggetti a cui viene applicato il materiale.

Le immagini esterne vengono memorizzate nella cache locale. Eventuali modifiche a tali immagini verranno rilevate solo dopo che la voce della cache locale diventa obsoleta (in base all’intestazione HTTP scadente).
