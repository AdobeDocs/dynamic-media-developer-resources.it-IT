---
title: Cache dei dati di risposta
description: ' [!DNL Platform Server] memorizza nella cache su disco tutte le immagini di risposta e alcuni dati di testo, a meno che una richiesta non sia contrassegnata come non memorizzabile in cache.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
TQID: 'https://experienceleague.adobe.com/zxZqRHFCMKKDxOBb35IEZWEhTFhknDgCKcYatA6lqGs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 282
ht-degree: 0%

---

# Cache dei dati di risposta{#response-data-cache}

[!DNL Platform Server] memorizza nella cache su disco tutte le immagini di risposta e alcuni dati di testo, a meno che una richiesta non sia contrassegnata come non memorizzabile in cache.

Il percorso della cache del disco di [!DNL Platform Server] è impostato con `PS::cache.rootPaths`.

Per le applicazioni con elevate percentuali di hit della cache, è possibile aumentare le prestazioni e la capacità del server distribuendo la cache dei dati di risposta tra più dispositivi disco. A tale scopo, creare una cartella radice della cache su ciascun disco e registrarla in `PS::cache.rootPaths`.

`PS::cache.maxSize` specifica la dimensione totale di tutte le voci della cache, senza considerare il sovraccarico del file system. La quantità di spazio su disco necessario dipende dalle proprietà del file system, ad esempio la dimensione del blocco del disco, e dal numero di voci della cache. Riserva il doppio dello spazio su disco per la cache del disco HTTP rispetto alla quantità specificata da `PS::cache.maxSize`. Per mantenere la quantità di dati memorizzati nella cache entro il limite, viene utilizzato un algoritmo utilizzato meno di recente.

Oltre a `PS::cache.maxSize`, la cache di risposta viene gestita anche limitando il numero massimo di voci della cache con `PS::cache.maxEntries`. In Linux®, questa impostazione deve specificare un valore non superiore al numero di nodi disponibili nella partizione della cache.

>[!NOTE]
>
>[!DNL Platform Server] mantiene un indice della cache in memoria. La dimensione dell&#39;indice è 32 byte volte il valore di `PS::cache.maxEntries`. Se necessario, aumenta la dimensione dell&#39;heap [!DNL Platform Server] per includere cache più grandi.

Il sistema utilizza un file di indice della cache che viene salvato su disco quando il server viene arrestato in modo ordinato. In caso di eventi imprevisti, ad esempio un&#39;interruzione dell&#39;alimentazione, il file potrebbe non essere salvato. Inoltre, potrebbero essere necessari alcuni minuti perché [!DNL Platform Server] sia pronto.
