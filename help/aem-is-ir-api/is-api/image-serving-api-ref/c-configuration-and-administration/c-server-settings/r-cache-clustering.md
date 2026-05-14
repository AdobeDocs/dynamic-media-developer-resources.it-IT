---
description: Utilizzare queste impostazioni del server per il clustering della cache.
solution: Experience Manager
title: Clustering cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
TQID: 'https://experienceleague.adobe.com/4SJmK1ILgnCBqYjjQcEnz0SVRzQfsY9mD05Xpd1ssnw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 200
ht-degree: 0%

---

# Clustering cache{#cache-clustering}

Utilizzare queste impostazioni del server per il clustering della cache.

## PS::cacheCluster.hosts - Host {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Elenco di indirizzi IP, separati da punti e virgola. Includi gli indirizzi IP di tutti i server peer da cui questo host deve ottenere i dati della cache. L&#39;indirizzo IP dell&#39;host locale può essere incluso per comodità. In questo modo è possibile utilizzare le stesse impostazioni di configurazione per tutti i server del cluster.

## PS::cacheCluster.updateLocalCache - Aggiorna cache locale {#section-154c2c0af4544200a3499232bb130dde}

Impostare su &#39;Sì&#39; se una voce della cache fornita da un server peer deve essere copiata nella cache di risposta locale.

## PS::cacheCluster.queryTimeout - Timeout query {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Quando si richiede una voce della cache dai server peer, il server attende che un server risponda che ha questo particolare elemento di dati o che tutti i server peer abbiano risposto che non hanno l&#39;elemento di dati o che il tempo specificato con questa impostazione (in millisecondi) sia scaduto.

## PS::cacheCluster.fetchTimeout - Recupera timeout {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Specifica il numero massimo di millisecondi di attesa del server per la consegna dei dati della cache effettivi dal server peer. Se i dati completi non sono stati consegnati prima della scadenza del timeout, il server presuppone che il peer non sia più disponibile. La voce della cache viene quindi generata localmente.
