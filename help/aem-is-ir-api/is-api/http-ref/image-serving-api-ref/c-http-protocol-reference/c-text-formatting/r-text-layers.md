---
description: textPs= supporta diversi modelli di utilizzo descritti in questa sezione.
seo-description: textPs= supporta diversi modelli di utilizzo descritti in questa sezione.
seo-title: Livelli di testo
solution: Experience Manager
title: Livelli di testo
topic: Scene7 Image Serving - Image Rendering API
uuid: 9ccef969-7c54-49ce-b6ff-ae4eabfcf99b
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 0%

---


# Livelli di testo{#text-layers}

textPs= supporta diversi modelli di utilizzo descritti in questa sezione.

>[!NOTE]
>
>Questa sezione non si applica a `text=`.

Regole e definizioni comuni sono le seguenti:

* I livelli di testo con ridimensionamento automatico sono livelli che non includono un comando `size=` o per i quali è specificato `size=0,0`.

* La dimensione del livello dei livelli di testo con ridimensionamento automatico è determinata dal testo effettivamente visualizzato.
* L’ancoraggio predefinito del livello dei livelli di testo con ridimensionamento automatico in genere è *not* al centro del livello (vedere di seguito).
* Se per i livelli di testo con ridimensionamento automatico è specificato `anchor=` o `origin=`, la posizione del livello di testo dipende dal contenuto del testo.

* Quando si specifica `size=`, è possibile eseguire il rendering di parti di glifi di caratteri all’esterno del rettangolo del livello.
* `pos=` può essere usato in tutti i casi per riposizionare un livello di testo.

## Testo punto (ridimensionamento automatico) {#section-db99ec98eb114458b2dbc9911a58f74a}

Il testo punto in stile Photoshop viene simulato quando `textPs=` viene specificato senza `size=`, `textPath=` o `textFlowPath=`. Le dimensioni del livello sono determinate orizzontalmente dalla larghezza del testo di cui è stato effettuato il rendering e verticalmente dall’interlinea. Il testo non va mai a capo automaticamente.

Se non vengono specificati né `anchor=` né `origin=`, la prima riga del testo viene posizionata immediatamente sopra l’origine del livello; i paragrafi contrassegnati con `\ql` sono posizionati a destra dell’origine del livello, i paragrafi che includono `\qr` vengono sottoposti a rendering a sinistra dell’origine e i paragrafi con `\qc` sono centrati orizzontalmente intorno all’origine. Le regole di posizionamento del livello standard si applicano se sono specificati `anchor=` o `origin=`.

Se si specifica `color=`, viene riempito il riquadro di delimitazione del testo effettivamente rappresentato.

I seguenti comandi RTF vengono ignorati: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Casella di testo rettangolare {#section-1d3ab11df26d4004a1a801546756475d}

Se `size=` è specificato oltre a `textPs=` (senza `textPath=` e `textFlowPath=`), il testo è vincolato al rettangolo specificato. Il livello viene posizionato come al solito. I glifi dei caratteri vicino ai bordi delle caselle di testo possono essere rappresentati parzialmente all’esterno della casella di testo.

`color=` riempie la regione definita da  `size=`.

Tutti i comandi RTF vengono applicati come previsto.

## Casella di testo altezza variabile {#section-e1233d1c9f8e43218667361dc0c4fd06}

Specificando `size=` con un&#39;altezza pari a 0, la casella di testo può essere ridimensionata verticalmente per contenere tutti i contenuti. La larghezza del livello è definita dalla larghezza di `size=` e l’altezza del livello dall’altezza del testo di cui è stato effettuato il rendering. Il livello viene posizionato come al solito. I glifi dei caratteri vicino ai bordi sinistro e destro della casella di testo possono essere rappresentati parzialmente all’esterno della casella di testo.

`color=` riempie il rettangolo definito dalla larghezza specificata  `size=` e dall’altezza del testo effettivo di cui è stato effettuato il rendering.

I seguenti comandi RTF vengono ignorati:

`\vertal*`

## Testo con ridimensionamento automatico nel percorso {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` insieme a  `textPs=` possono essere utilizzate per definire una o più aree in cui il testo deve essere scorrevole. `textFlowXPath=` può essere specificato facoltativamente per escludere il testo dallo scorrimento in una o più aree. Se `size=` non è specificato, il livello di testo risultante si ridimensiona automaticamente e la dimensione del livello è determinata dal riquadro di delimitazione del testo effettivamente rappresentato.

Se non vengono specificati né `origin=` né `anchor=`, per impostazione predefinita l’ancoraggio del livello corrisponde a (0,0) dello spazio delle coordinate pixel utilizzato per definire i tracciati, garantendo il posizionamento assoluto indipendentemente dal testo di cui è stato effettuato il rendering. Se si specifica `anchor=` o `origin=`, il livello viene posizionato in relazione al rettangolo di selezione del contenuto effettivo rappresentato e adattato al medesimo.

`color=` riempie il rettangolo di selezione del testo effettivo di cui è stato effettuato il rendering.

I seguenti comandi RTF vengono ignorati:

`\marg*`

## Testo predimensionato nel percorso {#section-ed492a8a54414cd4bde360500cec6968}

Se `size=` è specificato insieme a `textFlowPath=`, la dimensione del livello è predeterminata. 0,0 dello spazio di coordinate pixel utilizzato per definire i tracciati si trova nell’angolo superiore sinistro del rettangolo del livello.

Le aree `textFlowPath=` possono trovarsi all’esterno del rettangolo del livello. Il testo verrà sempre scorrevole ed eseguito il rendering in tutte le aree del tracciato, anche se questo comporta il rendering del testo all’esterno del rettangolo del livello. `extend=0,0,0,0`può essere usato per ritagliare il testo di cui è stato effettuato il rendering sul rettangolo del livello.

Ai fini del posizionamento del livello, il rettangolo del livello è basato sul `size=` specificato, indipendentemente dalla quantità di testo effettivamente rappresentata, anche se parte di esso si trova all’esterno del rettangolo del livello. Viene applicato il posizionamento standard del livello.

`color=` riempie l’area rettangolare definita da  `size=`.

I seguenti comandi RTF vengono ignorati per `textFlowPath=`:

`\marg*`

## Testo con ridimensionamento automatico sul percorso {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definisce uno o più percorsi sui quali  `textPs=` deve essere eseguito il rendering del testo specificato con. Se `size=` non è specificato, il livello di testo risultante si sta ridimensionando automaticamente. Le dimensioni del livello sono determinate dal rettangolo di selezione del testo effettivo su cui è stato effettuato il rendering.

Se non vengono specificati né `origin=` né `anchor=`, per impostazione predefinita l’ancoraggio del livello corrisponde a (0,0) dello spazio delle coordinate pixel utilizzato per definire il tracciato; la posizione del testo di cui è stato effettuato il rendering è fissa, indipendentemente dalla quantità di testo di cui è stato effettuato il rendering. Se si specifica `anchor=` o `origin=`, il livello viene posizionato in relazione al rettangolo di selezione del contenuto effettivo rappresentato e adattato al medesimo.

`color=` riempie il rettangolo di selezione del testo effettivo di cui è stato effettuato il rendering.

I seguenti comandi RTF vengono ignorati:

* `\marg*`
* `\hyph*`
* `\vertal*`

Qualsiasi testo dopo il primo `\par` o `\line` viene ignorato.

## Testo predimensionato sul percorso {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Se `size=` è specificato insieme a `textPath=`, la dimensione del livello è predeterminata. 0,0 dello spazio di coordinate pixel utilizzato per definire i tracciati si trova nell’angolo superiore sinistro del rettangolo del livello.

I tracciati possono essere posizionati parzialmente o interamente all’esterno del rettangolo del livello. Il testo verrà sempre applicato e rappresentato lungo l’intero tracciato, anche all’esterno del rettangolo del livello. `extend=0,0,0,0` può essere usato per ritagliare il testo di cui è stato effettuato il rendering sul rettangolo del livello.

Ai fini del posizionamento del livello, il rettangolo del livello è basato sul `size=` specificato, anche se viene eseguito il rendering di parte del testo all’esterno del rettangolo del livello. Viene applicato il posizionamento standard del livello.

`color=` riempie l&#39;area definita da  `size=`.

I seguenti comandi RTF vengono ignorati:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Qualsiasi testo dopo il primo `\par` o `\line` viene ignorato.
