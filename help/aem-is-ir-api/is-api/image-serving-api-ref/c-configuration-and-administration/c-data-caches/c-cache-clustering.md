---
description: Il clustering della cache consente a più server con carico bilanciato di scambiare le voci della cache nella cache di risposta principale e nella cache dei dati secondaria (per richieste nidificate/incorporate), con il potenziale di aumentare significativamente la reattività del server eliminando la necessità di generare la stessa voce della cache su più server.
solution: Experience Manager
title: Clustering cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Clustering cache{#cache-clustering}

Il clustering della cache consente a più server con carico bilanciato di scambiare le voci della cache nella cache di risposta principale e nella cache dei dati secondaria (per richieste nidificate/incorporate), con il potenziale di aumentare significativamente la reattività del server eliminando la necessità di generare la stessa voce della cache su più server.

Se configurata in questo modo, quando un server riceve una richiesta per un elemento che non si trova nella cache locale, contatta i server peer nel cluster. Prima di richiedere al server immagini di generare l&#39;elemento, verifica se l&#39;elemento dati è già presente.

Il clustering della cache è utile principalmente per le applicazioni che utilizzano contenuti altamente memorizzabili nella cache. I carichi del server devono essere ridotti in modo significativo durante la distribuzione iniziale e quando si entra in funzione con nuovi contenuti.

I timeout e altre protezioni garantiscono che il sistema continui a funzionare a piena capacità anche quando uno o più server peer sono offline.

Il cluster di cache può funzionare in una delle due configurazioni di base seguenti:

* Quando `PS::cacheCluster.updateLocalCache` è abilitato (impostazione predefinita), tutte le voci della cache trovate in un server peer vengono copiate nella cache locale.

  Questa configurazione riduce il traffico tra i server peer. Offre inoltre tempi di risposta più rapidi, a scapito della replica di tutte le voci della cache su tutti i server del cluster. Questa è la configurazione consigliata.

* Quando `PS::cacheCluster.updateLocalCache` è disabilitato, i dati provenienti da altri server non vengono copiati nella cache locale.

  Questo moltiplica lo spazio su disco disponibile per i dati della cache. Tuttavia, aumenta il traffico tra i server peer e riduce i tempi di risposta complessivi. Utilizza questa configurazione solo quando la percentuale di riscontri nella cache è bassa.
