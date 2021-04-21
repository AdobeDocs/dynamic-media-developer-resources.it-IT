---
description: Il clustering della cache consente a più server con carico bilanciato di scambiare voci di cache nella cache di risposta primaria e nella cache di dati secondaria (per le richieste nidificate/incorporate), con il potenziale di aumentare significativamente la reattività del server eliminando la necessità di generare la stessa voce di cache su più server.
solution: Experience Manager
title: Clustering cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# Clustering cache{#cache-clustering}

Il clustering della cache consente a più server con carico bilanciato di scambiare voci di cache nella cache di risposta primaria e nella cache di dati secondaria (per le richieste nidificate/incorporate), con il potenziale di aumentare significativamente la reattività del server eliminando la necessità di generare la stessa voce di cache su più server.

In tal caso, quando un server riceve una richiesta per un elemento che non si trova nella cache locale, contatta i server peer del cluster. Controlla se dispongono già di tale elemento prima di chiedere al server di immagini di generarlo.

Il clustering della cache offre soprattutto applicazioni che coinvolgono contenuti altamente memorizzabili nella cache. I carichi del server devono essere significativamente ridotti durante l&#39;implementazione iniziale e quando si procede con nuovi contenuti.

I timeout e altre misure di protezione garantiscono che il sistema continui a funzionare a piena capacità anche quando uno o più server peer sono offline.

Il cluster di cache può funzionare in una delle due configurazioni di base:

* Quando `PS::cacheCluster.updateLocalCache` è abilitato (impostazione predefinita), qualsiasi voce di cache trovata su un server peer viene copiata nella cache locale.

   Questa configurazione riduce il traffico tra i server peer. Fornisce anche i tempi di risposta più rapidi a costo di avere tutte le voci di cache replicate su tutti i server del cluster. Questa è la configurazione consigliata.

* Quando `PS::cacheCluster.updateLocalCache` è disabilitato, i dati provenienti da altri server non vengono copiati nella cache locale.

   Questo moltiplica lo spazio su disco disponibile per i dati della cache. Tuttavia, aumenta il traffico tra i server peer e riduce i tempi di risposta generali. Utilizza questa configurazione solo quando visualizzi percentuali di hit della cache basse.

