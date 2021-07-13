---
description: Platform Server memorizza in cache su disco tutte le immagini di risposta e alcuni dati di testo, a meno che una richiesta non sia contrassegnata come non memorizzabile in cache.
solution: Experience Manager
title: Cache dei dati di risposta
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Cache dei dati di risposta{#response-data-cache}

Platform Server memorizza in cache su disco tutte le immagini di risposta e alcuni dati di testo, a meno che una richiesta non sia contrassegnata come non memorizzabile in cache.

Il percorso della cache del disco del server Platform è impostato con `PS::cache.rootPaths`.

Per le applicazioni con elevate percentuali di hit della cache, è possibile aumentare le prestazioni e la capacità del server distribuendo la cache dei dati di risposta tra più dispositivi disco. A questo scopo, crea una cartella principale della cache su ciascun disco e registrale in `PS::cache.rootPaths`.

`PS::cache.maxSize` specifica la dimensione totale di tutte le voci della cache, senza considerare il sovraccarico del file system. La quantità di spazio su disco effettivamente necessaria dipende dalle proprietà del file system, come la dimensione del blocco del disco, e dal numero di voci della cache. Si consiglia di riservare alla cache del disco HTTP il doppio dello spazio su disco specificato da `PS::cache.maxSize`. Viene utilizzato un algoritmo meno recente per mantenere la quantità di dati memorizzati nella cache entro il limite.

Oltre a `PS::cache.maxSize`, la cache di risposta viene gestita anche limitando il numero massimo di voci di cache con `PS::cache.maxEntries`. Su Linux, questa impostazione deve specificare un valore non superiore al numero di nodi disponibili sulla partizione della cache.

>[!NOTE]
>
>Il server Platform mantiene un indice di cache in memoria. La dimensione di questo indice è 32 byte volte il valore di `PS::cache.maxEntries`. Potrebbe essere necessario aumentare le dimensioni dell’heap di Platform Server per contenere le cache più grandi.

Il sistema utilizza un file di indice della cache salvato su disco quando il server viene arrestato in modo ordinato. In caso di eventi imprevisti, ad esempio un&#39;interruzione dell&#39;alimentazione, è possibile che il file non venga salvato. Inoltre, potrebbero essere necessari diversi minuti perché Platform Server sia pronto.
