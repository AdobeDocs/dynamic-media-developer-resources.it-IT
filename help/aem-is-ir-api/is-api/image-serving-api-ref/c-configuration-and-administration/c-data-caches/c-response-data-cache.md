---
title: Cache dei dati di risposta
description: Il [!DNL Platform Server] memorizza nella cache su disco tutte le immagini di risposta e alcuni dati di testo, a meno che una richiesta non sia contrassegnata come non memorizzabile in cache.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Cache dei dati di risposta{#response-data-cache}

Il [!DNL Platform Server] memorizza nella cache su disco tutte le immagini di risposta e alcuni dati di testo, a meno che una richiesta non sia contrassegnata come non memorizzabile in cache.

La posizione del [!DNL Platform Server]La cache del disco di è impostata con `PS::cache.rootPaths`.

Per le applicazioni con elevate percentuali di hit della cache, è possibile aumentare le prestazioni e la capacità del server distribuendo la cache dei dati di risposta tra più dispositivi disco. A tale scopo, è necessario creare una cartella principale della cache su ciascun disco e registrarla in `PS::cache.rootPaths`.

Il `PS::cache.maxSize` specifica la dimensione totale di tutte le voci della cache, senza considerare il sovraccarico del file system. La quantità di spazio su disco necessario dipende dalle proprietà del file system, ad esempio la dimensione del blocco del disco, e dal numero di voci della cache. Riserva il doppio dello spazio su disco per la cache del disco HTTP rispetto alla quantità specificata da `PS::cache.maxSize`. Per mantenere la quantità di dati memorizzati nella cache entro il limite, viene utilizzato un algoritmo utilizzato meno di recente.

Oltre a `PS::cache.maxSize`, la cache di risposta viene gestita anche limitando il numero massimo di voci della cache con `PS::cache.maxEntries`. In Linux®, questa impostazione deve specificare un valore non superiore al numero di nodi disponibili nella partizione della cache.

>[!NOTE]
>
>Il [!DNL Platform Server] mantiene un indice della cache in memoria. La dimensione di questo indice è 32 byte volte il valore di `PS::cache.maxEntries`. Aumenta [!DNL Platform Server] dimensioni heap per adattarsi a cache più grandi, se necessario.

Il sistema utilizza un file di indice della cache che viene salvato su disco quando il server viene arrestato in modo ordinato. In caso di eventi imprevisti, ad esempio un&#39;interruzione dell&#39;alimentazione, il file potrebbe non essere salvato. Inoltre, potrebbero essere necessari alcuni minuti per [!DNL Platform Server] per prepararsi.
