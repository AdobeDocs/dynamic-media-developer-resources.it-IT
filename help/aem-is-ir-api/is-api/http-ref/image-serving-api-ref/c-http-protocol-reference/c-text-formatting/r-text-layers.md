---
description: textPs= supporta una serie di diversi modelli di utilizzo descritti in questa sezione.
solution: Experience Manager
title: Livelli di testo
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 0%

---


# Livelli di testo{#text-layers}

textPs= supporta una serie di diversi modelli di utilizzo descritti in questa sezione.

>[!NOTE]
>
>Questa sezione non si applica a `text=`.

Le regole e le definizioni comuni sono le seguenti:

* I livelli di testo con ridimensionamento automatico sono livelli che non includono un comando `size=` o per i quali è specificato `size=0,0`.

* Le dimensioni del livello dei livelli di testo con ridimensionamento automatico sono determinate dal testo effettivo renderizzato.
* L’ancoraggio predefinito dei livelli di testo con ridimensionamento automatico è generalmente *non* al centro del livello (vedi sotto).
* Se per i livelli di testo con ridimensionamento automatico è specificato `anchor=` o `origin=`, la posizione del livello di testo è influenzata dal contenuto del testo.

* Se si specifica `size=`, è possibile eseguire il rendering di parti di glifi di caratteri all&#39;esterno del rettangolo di livello.
* `pos=` può essere utilizzato in tutti i casi per riposizionare un livello di testo.

## Testo punto (ridimensionamento automatico) {#section-db99ec98eb114458b2dbc9911a58f74a}

Il testo punto in stile Photoshop viene simulato quando `textPs=` viene specificato senza `size=`, `textPath=` o `textFlowPath=`. La dimensione del livello viene determinata orizzontalmente in base alla larghezza del testo sottoposto a rendering e verticalmente in base all’interlinea. Il testo non si avvolgerà mai automaticamente.

Se non sono specificati né `anchor=` né `origin=`, la prima riga del testo viene posizionata immediatamente sopra l’origine del livello; i paragrafi contrassegnati con `\ql` sono posizionati a destra dell’origine del livello, i paragrafi che includono `\qr` vengono sottoposti a rendering a sinistra dell’origine e i paragrafi con `\qc` sono centrati orizzontalmente intorno all’origine. Le regole di posizionamento del livello standard si applicano se sono specificati `anchor=` o `origin=`.

Se è specificato `color=`, riempie il riquadro di delimitazione del testo effettivo renderizzato.

I seguenti comandi RTF vengono ignorati: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Casella di testo rettangolare {#section-1d3ab11df26d4004a1a801546756475d}

Se si specifica `size=` in aggiunta a `textPs=` (senza `textPath=` e `textFlowPath=`), il testo è vincolato al rettangolo specificato. Il livello viene posizionato come di consueto. È possibile eseguire il rendering dei glifi di carattere vicino ai bordi delle caselle di testo, in parte all’esterno della casella di testo.

`color=` riempie la regione definita da  `size=`.

Tutti i comandi RTF vengono applicati come previsto.

## Casella di testo a altezza variabile {#section-e1233d1c9f8e43218667361dc0c4fd06}

Specificando `size=` con altezza 0 la casella di testo può essere ridimensionata verticalmente per contenere tutti i contenuti. La larghezza del livello è definita dalla larghezza di `size=` e l&#39;altezza del livello dall&#39;altezza del testo renderizzato effettivo. Il livello viene posizionato come di consueto. È possibile eseguire il rendering dei glifi dei caratteri vicino ai bordi sinistro e destro della casella di testo, in parte all’esterno della casella di testo.

`color=` riempie il rettangolo definito dalla larghezza specificata con  `size=` e dall’altezza del testo effettivo renderizzato.

I seguenti comandi RTF vengono ignorati:

`\vertal*`

## Testo a ridimensionamento automatico nel percorso {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` insieme a  `textPs=` può essere utilizzato per definire una o più aree in cui il testo deve essere scorrevole. `textFlowXPath=` possono essere specificate facoltativamente per escludere il testo dallo scorrimento in una o più aree. Se `size=` non è specificato, il livello di testo risultante si ridimensiona automaticamente e le dimensioni del livello sono determinate dal riquadro di delimitazione del testo effettivamente sottoposto a rendering.

Se non vengono specificati né `origin=` né `anchor=`, l&#39;ancoraggio del livello viene impostato automaticamente su (0,0) dello spazio di coordinate pixel utilizzato per definire i percorsi, garantendo il posizionamento assoluto indipendentemente dal testo di cui è stato effettuato il rendering. Se sono specificati `anchor=` o `origin=`, il livello viene posizionato rispetto al riquadro di delimitazione del contenuto effettivo di cui è stato eseguito il rendering (e adattandolo ad esso).

`color=` riempie il riquadro di delimitazione del testo effettivo renderizzato.

I seguenti comandi RTF vengono ignorati:

`\marg*`

## Testo di dimensioni predefinite nel percorso {#section-ed492a8a54414cd4bde360500cec6968}

Se `size=` è specificato insieme a `textFlowPath=`, la dimensione del livello è predeterminata. (0,0) dello spazio di coordinate pixel utilizzato per definire i percorsi si trova nell&#39;angolo superiore sinistro del rettangolo di livello.

Le aree `textFlowPath=` possono essere situate al di fuori del rettangolo del livello. Il testo verrà sempre scorrevole ed eseguito il rendering in tutte le aree del tracciato, anche se questo comporta il rendering del testo al di fuori del rettangolo del livello. `extend=0,0,0,0`può essere utilizzato per ritagliare il testo di cui è stato eseguito il rendering sul rettangolo del livello.

A scopo di posizionamento del livello, il rettangolo del livello si basa sul `size=` specificato, indipendentemente dalla quantità di testo effettivamente renderizzato, anche se parte di esso si trova all’esterno del rettangolo del livello. Si applica il posizionamento standard del livello.

`color=` riempie l’area rettangolare definita da  `size=`.

I seguenti comandi RTF vengono ignorati per `textFlowPath=`:

`\marg*`

## Testo con ridimensionamento automatico sul percorso {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definisce uno o più percorsi in cui  `textPs=` deve essere eseguito il rendering del testo specificato con. Se `size=` non è specificato, il livello di testo risultante si ridimensiona automaticamente. La dimensione del livello è determinata dal riquadro di delimitazione del testo effettivo renderizzato.

Se non vengono specificati né `origin=` né `anchor=`, l&#39;ancoraggio del livello viene impostato automaticamente su (0,0) dello spazio di coordinate pixel utilizzato per definire il tracciato; la posizione del testo di cui è stato effettuato il rendering è fissa indipendentemente dalla quantità di testo di cui è stato eseguito il rendering. Se sono specificati `anchor=` o `origin=`, il livello viene posizionato rispetto al riquadro di delimitazione del contenuto effettivo di cui è stato eseguito il rendering (e adattandolo ad esso).

`color=` riempie il riquadro di delimitazione del testo effettivo renderizzato.

I seguenti comandi RTF vengono ignorati:

* `\marg*`
* `\hyph*`
* `\vertal*`

Qualsiasi testo dopo il primo `\par` o `\line` viene ignorato.

## Testo di dimensioni predefinite sul percorso {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Se `size=` è specificato insieme a `textPath=`, la dimensione del livello è predeterminata. (0,0) dello spazio di coordinate pixel utilizzato per definire i percorsi si trova nell&#39;angolo superiore sinistro del rettangolo di livello.

I percorsi possono essere posizionati parzialmente o interamente al di fuori del rettangolo del livello. Il testo viene sempre applicato ed eseguito il rendering lungo l’intero tracciato, anche all’esterno del rettangolo di livello. `extend=0,0,0,0` può essere utilizzato per ritagliare il testo di cui è stato eseguito il rendering sul rettangolo del livello.

A scopo di posizionamento del livello, il rettangolo del livello si basa sul `size=` specificato, anche se è eseguito il rendering di parte del testo all’esterno del rettangolo del livello. Si applica il posizionamento standard del livello.

`color=` riempie l’area definita da  `size=`.

I seguenti comandi RTF vengono ignorati:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Qualsiasi testo dopo il primo `\par` o `\line` viene ignorato.
