---
description: Crea un'applicazione a strati "bambola di carta".
solution: Experience Manager
title: Esempio C
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Esempio C{#example-c}

Crea un&#39;applicazione a strati &quot;bambola di carta&quot;.

Un&#39;immagine di sfondo contiene la foto di un modello o di un manichino. I record aggiuntivi nel catalogo delle immagini contengono vari capi di abbigliamento e accessori, fotografati per abbinare il manichino in forma e dimensione.

Ogni abbigliamento/foto accessorio viene mascherato e ritagliato al riquadro di delimitazione della maschera per ridurre al minimo le dimensioni dell&#39;immagine. Gli ancoraggi e le risoluzioni delle immagini sono attentamente controllati per mantenere l&#39;allineamento tra i livelli e l&#39;immagine di sfondo; tutte le immagini vengono aggiunte a un catalogo di immagini, con i valori appropriati memorizzati in `catalog::Resolution` e `catalog::Anchor`.

Oltre ai livelli, vogliamo anche modificare il colore per gli elementi selezionati. I record di questi elementi vengono preelaborati per rimuovere il colore originale e regolare la luminosità e il contrasto in modo adatto al comando di colorazione. Questa preelaborazione può essere eseguita offline, utilizzando uno strumento di modifica delle immagini come Photoshop, oppure, in casi semplici, può essere eseguita in modo banale aggiungendo `op_brightness=` e `op_contrast=` al campo `catalog::Modifier`.

Questa applicazione non richiede un modello separato, perché tutti gli oggetti sono già allineati correttamente dai relativi ancoraggi immagine ( `catalog::Anchor`) e ridimensionati ( `catalog::Resolution`). Lasciamo al cliente il compito di garantire un ordine appropriato dei livelli.

Una richiesta tipica potrebbe avere questo aspetto:

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Viene specificata solo l&#39;altezza. Questo consente all’immagine restituita di variare in larghezza a seconda delle proporzioni dell’immagine del manichino, senza riempire i margini con il colore di sfondo.

Non deve avere importanza quale risoluzione viene specificata per ogni livello, purché siano uguali. Questa versione potrebbe non consentire la visualizzazione di visualizzazioni più grandi delle immagini composite. Specificando un valore di risoluzione elevato si evitano problemi correlati a tale limite. Tutte le operazioni di elaborazione e composizione vengono eseguite alla risoluzione ottimale per le dimensioni dell&#39;immagine richieste, per ottenere prestazioni e qualità di output ottimali.

I comandi `res=` possono essere omessi se tutte le immagini di origine hanno la stessa risoluzione a scala completa (che è probabilmente il caso per questo tipo di applicazione).

È necessario specificare `rootId` per tutti i comandi `src=`, anche se sono uguali a `rootId` specificati nel percorso url.

Se non si utilizza alcun catalogo di immagini, non è possibile un approccio basato sulla risoluzione al ridimensionamento. In questo caso, i fattori di scala espliciti devono essere calcolati per ogni elemento di livello, in base al rapporto tra i valori `catalog::Resolution` di ciascun livello e il valore `catalog::Resolution` del livello di sfondo. La richiesta di composizione (con meno livelli) potrebbe quindi avere questo aspetto:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
