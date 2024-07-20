---
description: textPs= supporta diversi modelli di utilizzo descritti in questa sezione.
solution: Experience Manager
title: Livelli di testo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# Livelli di testo{#text-layers}

textPs= supporta diversi modelli di utilizzo descritti in questa sezione.

>[!NOTE]
>
>Questa sezione non si applica a `text=`.

Norme comuni e definizioni:

* I livelli di testo con ridimensionamento automatico sono livelli che non includono un comando `size=` o per i quali è specificato `size=0,0`.

* La dimensione del livello dei livelli di testo con ridimensionamento automatico è determinata dal testo effettivamente sottoposto a rendering.
* L&#39;ancoraggio predefinito dei livelli di testo con ridimensionamento automatico è generalmente *not* al centro del livello (vedi sotto).
* Se si specifica `anchor=` o `origin=` per i livelli di testo con ridimensionamento automatico, la posizione del livello di testo è influenzata dal contenuto del testo.

* Se si specifica `size=`, è possibile eseguire il rendering di parti dei glifi dei caratteri al di fuori del rettangolo del livello.
* `pos=` può essere utilizzato in tutti i casi per riposizionare un livello di testo.

## Testo punto (ridimensionamento automatico) {#section-db99ec98eb114458b2dbc9911a58f74a}

Il testo del punto in stile Photoshop viene simulato quando `textPs=` è specificato senza `size=`, `textPath=` o `textFlowPath=`. La dimensione del livello è determinata orizzontalmente dalla larghezza del testo sottoposto a rendering e verticalmente dall&#39;interlinea. Il testo non viene mai disposto automaticamente.

Se non si specificano né `anchor=` né `origin=`, la prima riga del testo viene posizionata immediatamente sopra l&#39;origine del livello; i paragrafi contrassegnati con `\ql` sono posizionati a destra dell&#39;origine del livello, i paragrafi che includono `\qr` vengono visualizzati a sinistra dell&#39;origine e i paragrafi con `\qc` sono centrati orizzontalmente intorno all&#39;origine. Le regole di posizionamento dei livelli standard si applicano se `anchor=` o `origin=` sono specificati.

Se si specifica `color=`, viene riempito il riquadro del testo di cui è stato eseguito il rendering.

I seguenti comandi RTF vengono ignorati: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Casella di testo rettangolare {#section-1d3ab11df26d4004a1a801546756475d}

Se `size=` è specificato in aggiunta a `textPs=` (senza `textPath=` e `textFlowPath=`), il testo è vincolato al rettangolo specificato. Il livello viene posizionato come di consueto. I glifi di caratteri accanto ai bordi della casella di testo possono essere visualizzati parzialmente all&#39;esterno della casella di testo.

`color=` riempie l&#39;area definita da `size=`.

Tutti i comandi RTF vengono applicati come previsto.

## Casella di testo Altezza variabile {#section-e1233d1c9f8e43218667361dc0c4fd06}

Se si specifica `size=` con altezza 0, la casella di testo può essere ridimensionata verticalmente per contenere tutto il contenuto. La larghezza del livello è definita dalla larghezza di `size=` e l&#39;altezza del livello dall&#39;altezza del testo di cui è stato eseguito il rendering. Il livello viene posizionato come di consueto. I glifi dei caratteri accanto ai bordi sinistro e destro della casella di testo possono essere visualizzati parzialmente all&#39;esterno della casella di testo.

`color=` riempie il rettangolo definito dalla larghezza specificata con `size=` e l&#39;altezza del testo effettivo sottoposto a rendering.

I seguenti comandi RTF vengono ignorati:

`\vertal*`

## Testo con ridimensionamento automatico nel percorso {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` in combinazione con `textPs=` può essere utilizzato per definire una o più aree in cui far scorrere il testo. È possibile specificare `textFlowXPath=` per escludere il testo dal flusso in una o più aree. Se `size=` non è specificato, il livello di testo risultante è di dimensioni autonome e la dimensione del livello è determinata dal riquadro di delimitazione del testo effettivamente sottoposto a rendering.

Se né `origin=` né `anchor=` sono specificati, l&#39;ancoraggio del livello utilizza per impostazione predefinita (0,0) lo spazio di coordinate pixel utilizzato per definire i percorsi, garantendo il posizionamento assoluto indipendentemente dal testo sottoposto a rendering. Se si specificano `anchor=` o `origin=`, il livello viene posizionato rispetto al rettangolo di selezione del contenuto effettivo sottoposto a rendering e si adatta a esso.

`color=` riempie il rettangolo di selezione del testo di cui è stato eseguito il rendering.

I seguenti comandi RTF vengono ignorati:

`\marg*`

## Testo pre-ridimensionato nel percorso {#section-ed492a8a54414cd4bde360500cec6968}

Se `size=` è specificato insieme a `textFlowPath=`, la dimensione del livello è predeterminata. (0,0) dello spazio di coordinate in pixel utilizzato per definire i tracciati si trova nell&#39;angolo superiore sinistro del rettangolo del livello.

Le aree `textFlowPath=` potrebbero trovarsi all&#39;esterno del rettangolo del livello. Il testo viene sempre riversato e sottoposto a rendering in tutte le aree del tracciato, anche se ciò comporta il rendering del testo al di fuori del rettangolo del livello. `extend=0,0,0,0` può essere utilizzato per ritagliare il testo di cui è stato eseguito il rendering nel rettangolo del livello.

Ai fini del posizionamento del livello, il rettangolo del livello è basato su `size=` specificato, indipendentemente dalla quantità di testo effettivamente sottoposto a rendering, anche se parte di esso si trova al di fuori del rettangolo del livello. Si applica il posizionamento del livello standard.

`color=` occupa l&#39;area rettangolare definita da `size=`.

I seguenti comandi RTF vengono ignorati per `textFlowPath=`:

`\marg*`

## Ridimensionamento automatico del testo nel percorso {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definisce uno o più percorsi in cui eseguire il rendering del testo specificato con `textPs=`. Se `size=` non è specificato, il livello di testo risultante sarà di dimensioni autonome. La dimensione del livello è determinata dal riquadro di delimitazione del testo effettivamente sottoposto a rendering.

Se né `origin=` né `anchor=` sono specificati, l&#39;ancoraggio del livello utilizza per impostazione predefinita (0,0) lo spazio di coordinate pixel utilizzato per definire il percorso; la posizione del testo sottoposto a rendering è fissa indipendentemente dalla quantità di testo sottoposto a rendering. Se si specificano `anchor=` o `origin=`, il livello viene posizionato rispetto al rettangolo di selezione del contenuto effettivo sottoposto a rendering e si adatta a esso.

`color=` riempie il rettangolo di selezione del testo di cui è stato eseguito il rendering.

I seguenti comandi RTF vengono ignorati:

* `\marg*`
* `\hyph*`
* `\vertal*`

Qualsiasi testo dopo il primo `\par` o `\line` viene ignorato.

## Testo pre-ridimensionato nel percorso {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Se `size=` è specificato insieme a `textPath=`, la dimensione del livello è predeterminata. (0,0) dello spazio di coordinate in pixel utilizzato per definire i tracciati si trova nell&#39;angolo superiore sinistro del rettangolo del livello.

I tracciati possono essere posizionati parzialmente o completamente all&#39;esterno del rettangolo del livello. Il testo viene sempre applicato e sottoposto a rendering lungo l&#39;intero tracciato, anche all&#39;esterno del rettangolo del livello. `extend=0,0,0,0` può essere utilizzato per ritagliare il testo di cui è stato eseguito il rendering nel rettangolo del livello.

Ai fini del posizionamento del livello, il rettangolo del livello si basa sul `size=` specificato, anche se parte del testo viene sottoposto a rendering all&#39;esterno del rettangolo del livello. Si applica il posizionamento del livello standard.

`color=` occupa l&#39;area definita da `size=`.

I seguenti comandi RTF vengono ignorati:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Qualsiasi testo dopo il primo `\par` o `\line` viene ignorato.
