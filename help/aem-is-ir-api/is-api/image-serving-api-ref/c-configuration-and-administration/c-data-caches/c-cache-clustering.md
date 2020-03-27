---
description: Il clustering della cache consente a più server bilanciati dal carico di scambiare le voci della cache nella cache delle risposte primarie e nella cache dei dati secondari (per le richieste nidificate/incorporate), con il potenziale di aumentare significativamente la reattività del server eliminando la necessità di generare la stessa voce della cache su più server.
seo-description: Il clustering della cache consente a più server bilanciati dal carico di scambiare le voci della cache nella cache delle risposte primarie e nella cache dei dati secondari (per le richieste nidificate/incorporate), con il potenziale di aumentare significativamente la reattività del server eliminando la necessità di generare la stessa voce della cache su più server.
seo-title: Clustering cache
solution: Experience Manager
title: Clustering cache
topic: Scene7 Image Serving - Image Rendering API
uuid: 347165d6-a9e7-406e-81a8-8a91f745ce27
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Clustering cache{#cache-clustering}

Il clustering della cache consente a più server bilanciati dal carico di scambiare le voci della cache nella cache delle risposte primarie e nella cache dei dati secondari (per le richieste nidificate/incorporate), con il potenziale di aumentare significativamente la reattività del server eliminando la necessità di generare la stessa voce della cache su più server.

In tal caso, quando un server riceve una richiesta per un elemento che non si trova nella cache locale, contatta i server peer del cluster. Controlla se dispongono già di tale elemento prima di chiedere al server immagini di generare l’elemento.

Il clustering della cache è principalmente utile per le applicazioni che richiedono contenuti altamente memorizzabili nella cache. I carichi sul server dovrebbero essere significativamente ridotti durante la distribuzione iniziale e quando si passa al vivo con nuovi contenuti.

Timeout e altre salvaguardie garantiscono che il sistema continui a funzionare a piena capacità anche quando uno o più server peer sono offline.

Il cluster di cache può funzionare in una delle due configurazioni di base:

* Quando `PS::cacheCluster.updateLocalCache` è abilitata (impostazione predefinita), qualsiasi voce della cache trovata in un server peer viene copiata nella cache locale.

   Questa configurazione riduce il traffico tra i server peer. Fornisce inoltre i tempi di risposta più rapidi al costo di far replicare tutte le voci della cache su tutti i server del cluster. Questa è la configurazione consigliata.

* Quando `PS::cacheCluster.updateLocalCache` è disattivato, i dati provenienti da altri server non vengono copiati nella cache locale.

   Questo moltiplica lo spazio disponibile su disco per i dati della cache. Tuttavia, aumenta il traffico tra i server peer e riduce i tempi di risposta complessivi. Utilizzate questa configurazione solo quando vengono visualizzate percentuali di hit della cache ridotte.

