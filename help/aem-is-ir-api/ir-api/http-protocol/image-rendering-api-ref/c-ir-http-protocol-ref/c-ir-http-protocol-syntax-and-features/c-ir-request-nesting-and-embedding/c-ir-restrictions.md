---
title: Restrizioni
description: Alcune restrizioni si applicano alla nidificazione e all’incorporamento.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
TQID: 'https://experienceleague.adobe.com/rwy6ZnKA0pc-z-dqhsI0gD-FSqpqZr1bcIgJqtsjfIs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 0%

---

# Restrizioni{#restrictions}

Alcune restrizioni si applicano alla nidificazione e all’incorporamento.

Per una buona performance del server, la risoluzione delle immagini restituite dalle richieste nidificate deve corrispondere ragionevolmente alla risoluzione della texture degli oggetti a cui viene applicato il materiale.

Le immagini esterne vengono memorizzate nella cache locale. Eventuali modifiche a tali immagini vengono rilevate solo dopo che la voce della cache locale diventa obsoleta (in base all’intestazione HTTP in scadenza).
