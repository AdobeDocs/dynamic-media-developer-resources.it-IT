---
description: Creare un'applicazione a livelli "carta bambola".
seo-description: Creare un'applicazione a livelli "carta bambola".
seo-title: Esempio C
solution: Experience Manager
title: Esempio C
topic: Scene7 Image Serving - Image Rendering API
uuid: 25f228c2-dc03-461a-aee8-40fdb3d4cf5e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# Esempio C{#example-c}

Creare un&#39;applicazione a livelli &quot;carta bambola&quot;.

Un&#39;immagine di sfondo contiene la foto di un modello o di un manichino. I record aggiuntivi nel catalogo delle immagini contengono vari capi di abbigliamento e accessori, fotografati per corrispondere al manichino in forma e dimensione.

Ogni abbigliamento/foto accessorio viene mascherato e ritagliato fino al rettangolo di selezione della maschera per ridurre al minimo le dimensioni dell’immagine. Gli ancoraggi e le risoluzioni delle immagini vengono controllati attentamente per mantenere l&#39;allineamento tra i livelli e l&#39;immagine di sfondo, e tutte le immagini vengono aggiunte a un catalogo di immagini, con i valori appropriati memorizzati in `catalog::Resolution` e `catalog::Anchor`.

Oltre ai livelli, è anche necessario modificare il colore per gli elementi selezionati. I record di questi elementi sono preelaborati per rimuovere il colore originale e regolare la luminosità e il contrasto in modo adatto per il comando colorizzazione. Questa preelaborazione può essere effettuata offline, utilizzando uno strumento di modifica delle immagini come Photoshop, oppure, in casi semplici, può essere eseguita in modo invisibile aggiungendo `op_brightness=` e `op_contrast=` al campo `catalog::Modifier`.

Questa applicazione non richiede un modello separato, perché tutti gli oggetti sono già allineati correttamente dai relativi ancoraggi di immagine ( `catalog::Anchor`) e ridimensionati ( `catalog::Resolution`). Lasciamo che sia il cliente a garantire l&#39;ordine appropriato dei livelli.

Una tipica richiesta potrebbe essere simile alla seguente:

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

È specificata solo l&#39;altezza. Questo consente all’immagine restituita di variare in larghezza a seconda delle proporzioni dell’immagine manichino, senza riempire i margini con il colore di sfondo.

Non deve essere importante quale risoluzione viene specificata per ciascun livello, purché siano tutte uguali. Questa versione potrebbe non consentire la visualizzazione di dimensioni maggiori rispetto alle immagini composite. Specificando un valore di risoluzione elevato si evitano problemi correlati a tale limitazione. Tutte le operazioni di elaborazione e composizione vengono eseguite alla risoluzione ottimale per le dimensioni dell&#39;immagine richieste, per ottenere prestazioni e qualità di output ottimali.

I comandi `res=` possono essere omessi se tutte le immagini di origine hanno la stessa risoluzione a scala intera (il che è probabile nel caso di questo tipo di applicazione).

È necessario specificare `rootId` per tutti i comandi `src=`, anche se sono identici a `rootId` specificati nel percorso url.

Se non si utilizza alcun catalogo immagini, non è possibile applicare il ridimensionamento in base alla risoluzione. In questo caso, è necessario calcolare i fattori di scala espliciti per ciascun elemento del livello, in base al rapporto tra i valori `catalog::Resolution` di ciascun livello e il valore `catalog::Resolution` del livello di sfondo. La richiesta di composizione (con un numero inferiore di livelli) potrebbe essere simile alla seguente:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

