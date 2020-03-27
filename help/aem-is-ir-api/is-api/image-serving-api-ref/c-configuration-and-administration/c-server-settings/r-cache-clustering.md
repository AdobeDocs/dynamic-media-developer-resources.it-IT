---
description: Utilizzate queste impostazioni del server per il clustering della cache.
seo-description: Utilizzate queste impostazioni del server per il clustering della cache.
seo-title: Clustering cache
solution: Experience Manager
title: Clustering cache
topic: Scene7 Image Serving - Image Rendering API
uuid: ed6335d7-26c9-45d8-95f6-6c05e788e449
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Clustering cache{#cache-clustering}

Utilizzate queste impostazioni del server per il clustering della cache.

## PS::cacheCluster.hosts - Host {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Elenco di indirizzi IP, separati da punto e virgola. Includete gli indirizzi IP di tutti i server peer da cui l&#39;host deve ottenere i dati della cache. L&#39;indirizzo IP dell&#39;host locale può essere incluso per comodità; questo consente le stesse impostazioni di configurazione per tutti i server del cluster.

## PS::cacheCluster.updateLocalCache - Aggiorna cache locale {#section-154c2c0af4544200a3499232bb130dde}

Impostate su &#39;Yes&#39; se una voce della cache fornita da un server peer deve essere copiata nella cache delle risposte locali.

## PS::cacheCluster.queryTimeout - Timeout query {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Quando si richiede una voce della cache dai server peer, il server attenderà fino a quando un server non risponderà che dispone di questo particolare elemento dati, o finché tutti i server peer non avranno risposto che non hanno l&#39;elemento dati, o fino a quando il tempo specificato con questa impostazione (in msec) non sarà scaduto.

## PS::cacheCluster.fetchTimeout - Timeout recupero {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Specifica il numero massimo di msec che il server attenderà che i dati effettivi della cache vengano inviati dal server peer. Se i dati completi non sono stati consegnati prima della scadenza del timeout, il server presume che il peer non sia più disponibile. La voce della cache viene quindi generata localmente.
