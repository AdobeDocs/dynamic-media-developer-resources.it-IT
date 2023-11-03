---
description: textPs= supporta diversi modelli di utilizzo descritti in questa sezione.
solution: Experience Manager
title: Livelli di testo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Livelli di testo{#text-layers}

textPs= supporta diversi modelli di utilizzo descritti in questa sezione.

>[!NOTE]
>
>Questa sezione non si applica a `text=`.

Norme comuni e definizioni:

* I livelli di testo con ridimensionamento automatico sono livelli che non includono `size=` comando o per il quale `size=0,0` è specificato.

* La dimensione del livello dei livelli di testo con ridimensionamento automatico è determinata dal testo effettivamente sottoposto a rendering.
* L&#39;ancoraggio di default dei livelli di testo con ridimensionamento automatico è generalmente *non* al centro del livello (vedere sotto).
* Se `anchor=` o `origin=` è specificato per i livelli di testo con ridimensionamento automatico; la posizione del livello di testo è influenzata dal contenuto del testo.

* Quando `size=` è specificato, parti dei glifi dei caratteri possono essere sottoposte a rendering al di fuori del rettangolo del livello.
* `pos=` può essere utilizzato in tutti i casi per riposizionare un livello di testo.

## Testo punto (ridimensionamento automatico) {#section-db99ec98eb114458b2dbc9911a58f74a}

Il testo del punto in stile Photoshop viene simulato quando `textPs=` è specificato senza `size=`, `textPath=`, o `textFlowPath=`. La dimensione del livello è determinata orizzontalmente dalla larghezza del testo sottoposto a rendering e verticalmente dall&#39;interlinea. Il testo non viene mai disposto automaticamente.

Se nessuno dei due `anchor=` né `origin=` vengono specificati, la prima riga del testo viene posizionata immediatamente sopra l&#39;origine del livello; i paragrafi contrassegnati con `\ql` sono posizionate a destra dell&#39;origine del livello, ovvero i paragrafi che includono `\qr` vengono visualizzati a sinistra dell’origine e i paragrafi con `\qc` sono centrati orizzontalmente intorno all’origine. Le regole di posizionamento del livello standard si applicano se `anchor=` o `origin=` sono specificati.

Se `color=` viene specificata, riempie il riquadro di delimitazione del testo effettivamente sottoposto a rendering.

I seguenti comandi RTF vengono ignorati: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Casella di testo rettangolare {#section-1d3ab11df26d4004a1a801546756475d}

Se `size=` è specificato in aggiunta a `textPs=` (senza `textPath=` e `textFlowPath=`), il testo è vincolato al rettangolo specificato. Il livello viene posizionato come di consueto. I glifi di caratteri accanto ai bordi della casella di testo possono essere visualizzati parzialmente all&#39;esterno della casella di testo.

`color=` riempie l&#39;area definita da `size=`.

Tutti i comandi RTF vengono applicati come previsto.

## Casella di testo Altezza variabile {#section-e1233d1c9f8e43218667361dc0c4fd06}

Specifica `size=` con altezza 0 consente di ridimensionare la casella di testo verticalmente per adattarla a tutto il contenuto. La larghezza del livello è definita dalla larghezza di `size=`e l&#39;altezza del livello in base all&#39;altezza del testo di cui è stato eseguito il rendering. Il livello viene posizionato come di consueto. I glifi dei caratteri accanto ai bordi sinistro e destro della casella di testo possono essere visualizzati parzialmente all&#39;esterno della casella di testo.

`color=` riempie il rettangolo definito dalla larghezza specificata con `size=` e l’altezza del testo effettivo sottoposto a rendering.

I seguenti comandi RTF vengono ignorati:

`\vertal*`

## Testo con ridimensionamento automatico nel percorso {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` in combinazione con `textPs=` può essere utilizzato per definire una o più aree in cui far scorrere il testo. `textFlowXPath=` può essere specificato facoltativamente per impedire al testo di scorrere in una o più aree. Se `size=` non è specificato, il livello di testo risultante è autodimensionato e la dimensione del livello è determinata dal riquadro di delimitazione del testo effettivamente sottoposto a rendering.

Se nessuno dei due `origin=` né `anchor=` se specificate, l&#39;ancoraggio del livello viene impostato automaticamente su (0,0) dello spazio di coordinate in pixel utilizzato per definire i percorsi, garantendo un posizionamento assoluto indipendentemente dal testo sottoposto a rendering. Se `anchor=` o `origin=` sono specificate, il livello viene posizionato rispetto al riquadro di delimitazione del contenuto effettivo sottoposto a rendering e si adatta a esso.

`color=` riempie il riquadro limite del testo di cui è stato eseguito il rendering.

I seguenti comandi RTF vengono ignorati:

`\marg*`

## Testo pre-ridimensionato nel percorso {#section-ed492a8a54414cd4bde360500cec6968}

Se `size=` è specificato insieme a `textFlowPath=`, la dimensione del livello è predeterminata. (0,0) dello spazio di coordinate in pixel utilizzato per definire i tracciati si trova nell&#39;angolo superiore sinistro del rettangolo del livello.

Il `textFlowPath=` le aree possono essere posizionate all&#39;esterno del rettangolo del livello. Il testo viene sempre riversato e sottoposto a rendering in tutte le aree del tracciato, anche se ciò comporta il rendering del testo al di fuori del rettangolo del livello. `extend=0,0,0,0`può essere utilizzato per ritagliare il testo sottoposto a rendering nel rettangolo del livello.

Ai fini del posizionamento del livello, il rettangolo del livello si basa sul valore specificato `size=`, indipendentemente dalla quantità di testo effettivamente sottoposto a rendering, anche se parte di esso si trova al di fuori del rettangolo del livello. Si applica il posizionamento del livello standard.

`color=` riempie l&#39;area rettangolare definita da `size=`.

I seguenti comandi RTF vengono ignorati per `textFlowPath=`:

`\marg*`

## Ridimensionamento automatico del testo nel percorso {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definisce uno o più percorsi in cui il testo specificato con `textPs=` deve essere renderizzato. Quando `size=` non è specificato, il livello di testo risultante è di dimensione automatica. La dimensione del livello è determinata dal riquadro di delimitazione del testo effettivamente sottoposto a rendering.

Se nessuno dei due `origin=` né `anchor=` se specificate, l&#39;ancoraggio del livello viene impostato automaticamente su (0,0) dello spazio di coordinate in pixel utilizzato per definire il tracciato; la posizione del testo sottoposto a rendering è fissa indipendentemente dalla quantità di testo sottoposto a rendering. Se `anchor=` o `origin=` sono specificate, il livello viene posizionato rispetto al riquadro di delimitazione del contenuto effettivo sottoposto a rendering e si adatta a esso.

`color=` riempie il riquadro limite del testo di cui è stato eseguito il rendering.

I seguenti comandi RTF vengono ignorati:

* `\marg*`
* `\hyph*`
* `\vertal*`

Qualsiasi testo dopo il primo `\par` o `\line` viene ignorato.

## Testo pre-ridimensionato nel percorso {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Se `size=` è specificato insieme a `textPath=`, la dimensione del livello è predeterminata. (0,0) dello spazio di coordinate in pixel utilizzato per definire i tracciati si trova nell&#39;angolo superiore sinistro del rettangolo del livello.

I tracciati possono essere posizionati parzialmente o completamente all&#39;esterno del rettangolo del livello. Il testo viene sempre applicato e sottoposto a rendering lungo l&#39;intero tracciato, anche all&#39;esterno del rettangolo del livello. `extend=0,0,0,0` può essere utilizzato per ritagliare il testo sottoposto a rendering nel rettangolo del livello.

Ai fini del posizionamento del livello, il rettangolo del livello si basa sul valore specificato `size=`, anche se parte del testo viene riprodotto all&#39;esterno del rettangolo del livello. Si applica il posizionamento del livello standard.

`color=` riempie l&#39;area definita da `size=`.

I seguenti comandi RTF vengono ignorati:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Qualsiasi testo dopo il primo `\par` o `\line` viene ignorato.
