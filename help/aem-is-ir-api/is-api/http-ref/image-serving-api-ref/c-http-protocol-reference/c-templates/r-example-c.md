---
title: Esempio C
description: Creare un'applicazione di stratificazione per bambole di carta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Esempio C{#example-c}

Creare un&#39;applicazione di stratificazione per bambole di carta.

Un&#39;immagine di sfondo contiene la foto di un modello o manichino. Ulteriori registrazioni nel catalogo delle immagini contengono vari articoli di abbigliamento e accessori, fotografati per corrispondere al manichino in forma e dimensioni.

Ogni foto di abbigliamento/accessori viene mascherata e ritagliata in base al riquadro di delimitazione della maschera per ridurre al minimo le dimensioni dell&#39;immagine. Gli ancoraggi e le risoluzioni delle immagini sono attentamente controllati per mantenere l&#39;allineamento tra i livelli e l&#39;immagine di sfondo e tutte le immagini vengono aggiunte a un catalogo di immagini, con i valori appropriati memorizzati in `catalog::Resolution` e `catalog::Anchor`.

Oltre a creare livelli, è necessario modificare anche il colore degli elementi selezionati. I record di questi elementi vengono preelaborati per rimuovere il colore originale e regolare la luminosità e il contrasto in modo adatto al comando di colorizzazione. Questa pre-elaborazione può essere eseguita off-line, utilizzando uno strumento di modifica delle immagini come Adobe Photoshop oppure, in casi semplici, aggiungendo `op_brightness=` e `op_contrast=` al `catalog::Modifier`campo.

Questa applicazione non richiede un modello separato, perché tutti gli oggetti sono già correttamente allineati dai relativi ancoraggi immagine ( `catalog::Anchor`) e ridimensionati ( `catalog::Resolution`). È compito del client garantire un ordine dei livelli appropriato.

Una richiesta tipica potrebbe essere simile alla seguente:

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Viene specificata solo l&#39;altezza. In questo modo l&#39;immagine restituita può variare in larghezza a seconda delle proporzioni dell&#39;immagine del manichino, senza riempire i margini con il colore di sfondo.

Non dovrebbe avere importanza quale risoluzione viene specificata per ogni livello, purché siano tutte uguali. Questa versione non consente di ingrandire le visualizzazioni rispetto alle immagini composite. Specificando un valore di risoluzione elevato si evitano i problemi correlati a questa limitazione. Tutte le operazioni di elaborazione e composizione vengono eseguite alla risoluzione ottimale per le dimensioni dell&#39;immagine richieste, in modo da ottenere prestazioni e qualità di output ottimali.

Il `res=` i comandi possono essere omessi se tutte le immagini sorgente hanno la stessa risoluzione a scala intera (come probabilmente avviene per questo tipo di applicazione).

Il `rootId` deve essere specificato per tutti `src=` , anche se sono uguali ai comandi `rootId` specificato nel percorso url.

Se non deve essere utilizzato alcun catalogo di immagini, non è possibile adottare un approccio di ridimensionamento basato sulla risoluzione. In questo caso, è necessario calcolare fattori di scala espliciti per ogni elemento di livello, in base al rapporto tra `catalog::Resolution` valori per ciascun livello al `catalog::Resolution` valore del livello di sfondo. La richiesta di composizione (con un numero inferiore di livelli) potrebbe quindi essere simile alla seguente:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
