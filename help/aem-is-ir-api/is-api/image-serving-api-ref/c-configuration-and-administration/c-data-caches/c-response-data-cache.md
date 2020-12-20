---
description: Il server piattaforma memorizza in cache su disco tutte le immagini di risposta e alcuni dati di testo, a meno che una richiesta non sia contrassegnata come non memorizzabile nella cache.
seo-description: Il server piattaforma memorizza in cache su disco tutte le immagini di risposta e alcuni dati di testo, a meno che una richiesta non sia contrassegnata come non memorizzabile nella cache.
seo-title: Cache dei dati di risposta
solution: Experience Manager
title: Cache dei dati di risposta
topic: Scene7 Image Serving - Image Rendering API
uuid: dbfda210-3b50-4e8c-8d77-7263ae4e80a2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Cache dei dati di risposta{#response-data-cache}

Il server piattaforma memorizza in cache su disco tutte le immagini di risposta e alcuni dati di testo, a meno che una richiesta non sia contrassegnata come non memorizzabile nella cache.

Il percorso della cache del disco del server della piattaforma è impostato con `PS::cache.rootPaths`.

Per le applicazioni con elevate frequenze di hit della cache, potete aumentare le prestazioni e la capacità del server distribuendo la cache dei dati di risposta tra più dispositivi disco. A tal fine, create una cartella cache root su ciascun disco e registratele in `PS::cache.rootPaths`.

`PS::cache.maxSize` specifica la dimensione totale di tutte le voci della cache, senza considerare il sovraccarico del file system. La quantità di spazio su disco effettivamente necessaria dipende dalle proprietà del file system, come la dimensione del blocco del disco, e dal numero di voci della cache. Si consiglia di riservare il doppio dello spazio su disco per la cache del disco HTTP rispetto alla quantità specificata da `PS::cache.maxSize`. Viene utilizzato un algoritmo meno recente per mantenere la quantità di dati memorizzati nella cache entro il limite.

Oltre a `PS::cache.maxSize`, la cache delle risposte viene gestita anche limitando il numero massimo di voci della cache con `PS::cache.maxEntries`. In Linux, questa impostazione deve specificare un valore non superiore al numero di nodi disponibili nella partizione della cache.

>[!NOTE]
>
>Il server piattaforma mantiene un indice della cache in memoria. La dimensione di questo indice è 32 byte volte il valore di `PS::cache.maxEntries`. Potrebbe essere necessario aumentare le dimensioni dell&#39;heap del server piattaforma per contenere cache più grandi.

Il sistema utilizza un file di indice della cache che viene salvato su disco quando il server viene spento in modo ordinato. In caso di eventi imprevisti come un&#39;interruzione di corrente, il file potrebbe non essere salvato. Inoltre, potrebbero essere necessari alcuni minuti perché il server della piattaforma sia pronto.
