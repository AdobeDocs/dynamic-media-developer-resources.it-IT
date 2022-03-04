---
title: Vignettature
description: Le vignette sono immagini create con Dynamic Media Image Authoring per l’utilizzo con Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e1be99c-58c0-4e3c-bc57-7be5fa25ccef
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Vignettature{#vignettes}

Le vignette sono immagini create con Dynamic Media Image Authoring per l’utilizzo con Image Rendering.

IR supporta due tipi di vignettatura di base: *2D* e *3D*. Le scene delle stanze sono solitamente vignette 3D che possono riprodurre riflessi, mentre la maggior parte delle altre scene, come abbigliamento o tappezzeria, sono di norma vignette 2D che non hanno capacità di rendering del riflesso.

Le vignette contengono un *visualizzare* e una gerarchia *oggetti*.

La visualizzazione è il contenitore dell&#39;immagine principale, mappe di illuminazione condivise, mappe di riflessione condivise e altri dati associati all&#39;intera immagine.

La gerarchia degli oggetti è costituita da *gruppi di oggetti*, *oggetti standard* e *sovrapporre gli oggetti*.

Ogni oggetto standard controlla un&#39;area dell&#39;immagine di visualizzazione, definita con una scala di grigi *maschera*. Le maschere degli oggetti standard non si sovrappongono mai. Gli oggetti standard non possono essere nascosti direttamente, ma possono essere coperti parzialmente o interamente da oggetti sovrapposti. La maggior parte o tutti gli oggetti di una vignetta tipica sono oggetti standard.

Sovrapponi gli oggetti posizionati sopra l&#39;immagine di visualizzazione e l&#39;uno sull&#39;altro. L’ordine di sovrapposizione è definito da un valore z assegnato all’oggetto. Gli oggetti di sovrapposizione sono utili quando le parti di una scena devono essere mostrate o nascoste dinamicamente.

Sono supportati diversi tipi di oggetti (sia standard che sovrapposti), ciascuno con il proprio scopo distinto:

* **Oggetti planari** (in vignette 3D) e **oggetti piatti** (in vignette 2D) accettano materiali di texture ripetibili. Sono generalmente utilizzati per pavimenti, controsoffitti e altre superfici piane che richiedono solo la mappatura prospettica.
* **Oggetti flowline** mappare superfici curve di forma levigata, come la tappezzeria, e vengono utilizzati occasionalmente anche per oggetti di abbigliamento. Possono essere utilizzati sia nelle vignette 2D che 3D e, se completamente creati, partecipano al rendering dei riflessi.
* **Oggetti non testurabili** consentono solo la modifica del colore. Sono consentiti sia nelle vignette 2D che 3D. Sono intrinsecamente non testurabili oppure possono essere un oggetto planare o flowline con un flag speciale &#39;No Texture&#39; impostato. Questo metodo è utile nelle vignette 3D per consentire agli oggetti di partecipare al rendering del riflesso, anche se l&#39;oggetto accetta solo materiali a colori solidi.
* **Oggetti di sketch** sono più utilizzati per oggetti in tessuto con pieghe e rughe, come gli articoli di abbigliamento. Come gli oggetti flowline, possono essere utilizzati nelle vignette 2D e 3D, anche se l’applicazione nelle vignette 3D è limitata.
* **Oggetti a muro** sono simili agli oggetti planari e sono supportate solo nelle vignette 3D. Sono dotate di particolari informazioni di layout che consentono l&#39;applicazione di due diverse finiture per pareti (superiore e inferiore) e fino a tre materiali per il bordo della parete. Quando viene creata correttamente, i materiali applicati ai muri scorrono accuratamente e senza soluzione di continuità tra muri adiacenti, per applicazioni realistiche di sfondo/bordo parete. Gli oggetti parete non supportano la rotazione della texture.
* **Oggetti del cabinet** sono consentiti solo nelle vignette 3D. Sono utilizzati per l&#39;authoring di armadi da cucina e da bagno con requisiti di layout complessi. Gli oggetti gabinetto accettano texture ripetibili e appositamente creati *file di stile archivio* contenente immagini del pannello mobile ridimensionabili.

Oltre ai tipi di oggetto di base, sono supportati due tipi speciali di oggetti di sovrapposizione:

* **Oggetti di sovrapposizione statici** sono oggetti che non accettano materiali. Sono consentiti sia nelle vignette 2D che 3D. Sono utili per gli accessori rimovibili in una scena della stanza, per le ombre cadenti dietro oggetti di sovrapposizione renderizzabili e applicazioni simili.
* **Oggetti frame della finestra** fornire informazioni di posizionamento per applicare i file di stile dei rivestimenti delle finestre, creati indipendentemente dalla vignetta e che possono essere condivisi tra le vignette.

Gli oggetti vengono raccolti in *gruppi di oggetti*, simile a un file system. Il raggruppamento si basa normalmente sulla struttura degli oggetti fisici che rappresentano (ad esempio, un gruppo &quot;Tutti gli armadi&quot; potrebbe contenere &quot;Cabinetti di base&quot; e &quot;Cabine di parete&quot;). È consentito qualsiasi numero di livelli di gruppo. Il raggruppamento supporta l&#39;applicazione di materiali a più oggetti simili.

* [Coordinate della scena](c-ir-scene-coordinates.md)
* [Risoluzione del materiale](c-ir-material-resolution.md)
