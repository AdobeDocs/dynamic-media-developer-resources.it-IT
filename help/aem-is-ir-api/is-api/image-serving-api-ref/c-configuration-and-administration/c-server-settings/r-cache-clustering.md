---
description: Utilizza queste impostazioni del server per il clustering cache.
solution: Experience Manager
title: Clustering cache
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Clustering cache{#cache-clustering}

Utilizza queste impostazioni del server per il clustering cache.

## PS::cacheCluster.hosts - Host {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Elenco di indirizzi IP separati da punti e virgola. Includi gli indirizzi IP di tutti i server peer da cui l’host deve ottenere i dati della cache. L&#39;indirizzo IP dell&#39;host locale può essere incluso per comodità; questo consente le stesse impostazioni di configurazione per tutti i server del cluster.

## PS::cacheCluster.updateLocalCache - Aggiorna la cache locale {#section-154c2c0af4544200a3499232bb130dde}

Imposta su &#39;Sì&#39; se una voce della cache fornita da un server peer deve essere copiata nella cache di risposta locale.

## PS::cacheCluster.queryTimeout - Timeout query {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Quando si richiede una voce di cache dai server peer, il server attenderà che un server risponda di avere questo particolare elemento di dati o finché tutti i server peer non avranno risposto di non disporre dell&#39;elemento di dati o finché non sarà scaduto il tempo specificato con questa impostazione (in msec).

## PS::cacheCluster.fetchTimeout - Timeout recupero {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Specifica il numero massimo di msec che il server attenderà che i dati della cache effettivi vengano inviati dal server peer. Se i dati completi non sono stati consegnati prima della scadenza del timeout, il server presuppone che il peer non sia più disponibile. La voce cache viene quindi generata localmente.
