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

* I livelli di testo con ridimensionamento automatico sono livelli che non includono un `size=` comando o per i quali `size=0,0` è specificato.

* La dimensione del livello dei livelli di testo con ridimensionamento automatico è determinata dal testo effettivamente visualizzato.
* L’ancoraggio predefinito del livello di ridimensionamento automatico dei livelli di testo *non* si trova al centro del livello (vedere di seguito).
* Se `anchor=` o `origin=` è specificato per il ridimensionamento automatico dei livelli di testo, la posizione del livello di testo dipende dal contenuto del testo.

* Quando `size=` viene specificato, al di fuori del rettangolo del livello è possibile eseguire il rendering di parti di glifi di caratteri.
* `pos=` può essere usato in tutti i casi per riposizionare un livello di testo.

## Testo punto (ridimensionamento automatico) {#section-db99ec98eb114458b2dbc9911a58f74a}

Il testo punto in stile Photoshop viene simulato se `textPs=` viene specificato senza `size=`, `textPath=`o `textFlowPath=`. Le dimensioni del livello sono determinate orizzontalmente dalla larghezza del testo di cui è stato effettuato il rendering e verticalmente dall’interlinea. Il testo non va mai a capo automaticamente.

Se non `anchor=` vengono specificati né `origin=` sono specificati, la prima riga del testo viene posizionata immediatamente sopra l’origine del livello; i paragrafi contrassegnati con `\ql` sono posizionati a destra dell’origine del livello, i paragrafi che includono `\qr` vengono sottoposti a rendering a sinistra dell’origine e i paragrafi con `\qc` esso sono centrati orizzontalmente intorno all’origine. Se `anchor=` o `origin=` sono specificate, si applicano le regole di posizionamento standard del livello.

Se `color=` viene specificato, riempie il riquadro di delimitazione del testo effettivo di cui è stato effettuato il rendering.

I seguenti comandi RTF vengono ignorati: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Casella di testo rettangolare {#section-1d3ab11df26d4004a1a801546756475d}

Se `size=` è specificato oltre a `textPs=` (senza `textPath=` e `textFlowPath=`), il testo è vincolato al rettangolo specificato. Il livello viene posizionato come al solito. I glifi dei caratteri vicino ai bordi delle caselle di testo possono essere rappresentati parzialmente all’esterno della casella di testo.

`color=` riempie la regione definita da `size=`.

Tutti i comandi RTF vengono applicati come previsto.

## Casella di testo Altezza variabile {#section-e1233d1c9f8e43218667361dc0c4fd06}

Specificando `size=` un valore di altezza pari a 0 la casella di testo può essere ridimensionata in verticale per contenere tutti i contenuti. La larghezza del livello è definita dalla larghezza `size=`e l’altezza del livello in base all’altezza del testo di cui è stato effettuato il rendering. Il livello viene posizionato come al solito. I glifi dei caratteri vicino ai bordi sinistro e destro della casella di testo possono essere rappresentati parzialmente all’esterno della casella di testo.

`color=` riempie il rettangolo definito dalla larghezza specificata con `size=` e l’altezza del testo effettivo rappresentato.

I seguenti comandi RTF vengono ignorati:

`\vertal*`

## Testo con ridimensionamento automatico nel percorso {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` in combinazione con `textPs=` può essere utilizzato per definire una o più aree in cui il testo deve essere scorrevole. `textFlowXPath=` può essere specificato facoltativamente per escludere il testo dallo scorrimento in una o più aree. Se non `size=` viene specificato, il livello di testo risultante si ridimensiona automaticamente e le dimensioni del livello sono determinate dal rettangolo di selezione del testo effettivamente rappresentato.

Se non `origin=` vengono specificati né `anchor=` sono specificati, l’ancoraggio del livello assume per impostazione predefinita (0,0) lo spazio delle coordinate pixel utilizzato per definire i tracciati, garantendo il posizionamento assoluto indipendentemente dal testo di cui è stato effettuato il rendering. Se `anchor=` o `origin=` sono specificati, il livello viene posizionato in relazione al rettangolo di selezione del contenuto effettivo su cui è stato effettuato il rendering.

`color=` riempie il rettangolo di selezione del testo effettivo di cui è stato effettuato il rendering.

I seguenti comandi RTF vengono ignorati:

`\marg*`

## Testo predimensionato nel percorso {#section-ed492a8a54414cd4bde360500cec6968}

Se `size=` viene specificato insieme a `textFlowPath=`, la dimensione del livello viene predeterminata. 0,0 dello spazio di coordinate pixel utilizzato per definire i tracciati si trova nell’angolo superiore sinistro del rettangolo del livello.

Le `textFlowPath=` aree possono essere esterne al rettangolo del livello. Il testo verrà sempre scorrevole ed eseguito il rendering in tutte le aree del tracciato, anche se questo comporta il rendering del testo all’esterno del rettangolo del livello. `extend=0,0,0,0`può essere usato per ritagliare il testo di cui è stato effettuato il rendering sul rettangolo del livello.

Ai fini del posizionamento del livello, il rettangolo del livello è basato sul valore specificato, indipendentemente dal testo effettivamente rappresentato, anche se parte di esso si trova all’esterno del rettangolo del livello. `size=` Viene applicato il posizionamento standard del livello.

`color=` riempie l’area rettangolare definita da `size=`.

I seguenti comandi RTF vengono ignorati per `textFlowPath=`:

`\marg*`

## Testo con ridimensionamento automatico sul tracciato {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definisce uno o più percorsi in cui `textPs=` deve essere rappresentato il testo specificato con. Se non `size=` viene specificato, il livello di testo risultante si ridimensiona automaticamente. Le dimensioni del livello sono determinate dal rettangolo di selezione del testo effettivo su cui è stato effettuato il rendering.

Se non `origin=` vengono specificati né `anchor=` sono specificati, l’ancoraggio del livello assume per impostazione predefinita (0,0) lo spazio delle coordinate pixel utilizzato per definire il tracciato; la posizione del testo di cui è stato effettuato il rendering è fissa, indipendentemente dalla quantità di testo di cui è stato effettuato il rendering. Se `anchor=` o `origin=` sono specificati, il livello viene posizionato in relazione al rettangolo di selezione del contenuto effettivo su cui è stato effettuato il rendering.

`color=` riempie il rettangolo di selezione del testo effettivo di cui è stato effettuato il rendering.

I seguenti comandi RTF vengono ignorati:

* `\marg*`
* `\hyph*`
* `\vertal*`

Qualsiasi testo dopo il primo `\par` o `\line` viene ignorato.

## Testo predimensionato sul percorso {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Se `size=` viene specificato insieme a `textPath=`, la dimensione del livello viene predeterminata. 0,0 dello spazio di coordinate pixel utilizzato per definire i tracciati si trova nell’angolo superiore sinistro del rettangolo del livello.

I tracciati possono essere posizionati parzialmente o interamente all’esterno del rettangolo del livello. Il testo verrà sempre applicato e rappresentato lungo l’intero tracciato, anche all’esterno del rettangolo del livello. `extend=0,0,0,0` può essere usato per ritagliare il testo di cui è stato effettuato il rendering sul rettangolo del livello.

Ai fini del posizionamento del livello, il rettangolo del livello è basato su uno specifico `size=`, anche se viene eseguito il rendering di parte del testo all’esterno del rettangolo del livello. Viene applicato il posizionamento standard del livello.

`color=` riempie l&#39;area definita da `size=`.

I seguenti comandi RTF vengono ignorati:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Qualsiasi testo dopo il primo `\par` o `\line` viene ignorato.
