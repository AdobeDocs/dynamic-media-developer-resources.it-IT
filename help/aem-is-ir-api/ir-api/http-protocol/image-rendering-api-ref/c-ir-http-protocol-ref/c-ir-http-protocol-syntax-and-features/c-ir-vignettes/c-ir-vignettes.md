---
title: Vignettature
description: Le vignettature sono immagini create con Dynamic Media Image Authoring e utilizzate con Image Rendering.
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

Le vignettature sono immagini create con Dynamic Media Image Authoring e utilizzate con Image Rendering.

IR supporta due tipi di vignettatura di base: *2D* e *3D*. Le scene delle stanze sono tipicamente vignettature 3D che possono riprodurre riflessi, mentre la maggior parte delle altre scene, come abbigliamento o tappezzeria, sono normalmente vignettature 2D che non hanno capacità di rendering dei riflessi.

Le vignette contengono una *vista* e una gerarchia di *oggetti*.

La vista è il contenitore dell&#39;immagine principale, delle mappe di illuminazione condivise, delle mappe di riflessione condivise e di altri dati associati all&#39;intera immagine.

La gerarchia degli oggetti è costituita da *gruppi di oggetti*, *oggetti standard* e *oggetti sovrapposti*.

Ogni oggetto standard controlla un&#39;area dell&#39;immagine di visualizzazione, definita con una *maschera* in scala di grigio. Le maschere degli oggetti standard non si sovrappongono mai. Gli oggetti standard non possono essere nascosti direttamente, ma possono essere coperti parzialmente o interamente da oggetti sovrapposti. La maggior parte o tutti gli oggetti di una vignettatura tipica sono oggetti standard.

Sovrapponi il livello degli oggetti sopra l&#39;immagine della vista e l&#39;uno con l&#39;altro. L&#39;ordine di sovrapposizione è definito da un valore z assegnato all&#39;oggetto. Gli oggetti di sovrapposizione sono utili quando è necessario visualizzare o nascondere dinamicamente parti di una scena.

Sono supportati diversi tipi di oggetti (standard e sovrapposizione), ciascuno con un proprio scopo distinto:

* **Gli oggetti planari** (nelle vignettature 3D) e **gli oggetti piatti** (nelle vignettature 2D) accettano materiali di texture ripetibili. Vengono in genere utilizzati per pavimenti, controsoffitti e altre superfici piane che richiedono solo la mappatura prospettica.
* **Gli oggetti con linea di flusso** consentono di mappare superfici curve di forma uniforme, ad esempio rivestimenti, e vengono utilizzati occasionalmente anche per gli oggetti di abbigliamento. Possono essere utilizzati sia nelle vignettature 2D che 3D e, se completamente creati, partecipano al rendering di riflessione.
* **Gli oggetti non testurizzabili** consentono solo le modifiche di colore. Sono consentite nelle vignettature 2D e 3D. Sono intrinsecamente non texturabili o possono essere un oggetto planare o di linea di flusso con uno speciale flag &quot;No Texture&quot; impostato. Questo metodo è utile nelle vignettature 3D per consentire agli oggetti di partecipare al rendering della riflessione, anche se l&#39;oggetto accetta solo materiali di colore solido.
* **Gli oggetti di sketch** vengono utilizzati in modo ottimale per gli oggetti di struttura con pieghe e rughe, ad esempio gli indumenti. Analogamente agli oggetti della linea di flusso, possono essere utilizzati nelle vignettature 2D e 3D, anche se l’applicazione nelle vignettature 3D è limitata.
* **Gli oggetti Wall** sono simili agli oggetti planari e sono supportati solo nelle vignettature 3D. Dispongono di informazioni di layout speciali che consentono l&#39;applicazione di due diverse finiture di parete (superiore e inferiore) e fino a tre materiali di bordo della parete. Se creati correttamente, i materiali applicati alle pareti scorrono in modo accurato e senza soluzione di continuità tra le pareti adiacenti, per applicazioni realistiche di carta da parati/bordi murali. Gli oggetti di parete non supportano la rotazione della texture.
* **Gli oggetti scaffale** sono consentiti solo nelle vignettature 3D. Sono utilizzati per creare armadi da cucina e da bagno con requisiti di layout complessi. Gli oggetti Cabinet accettano texture ripetibili e *file di stile file CAB* appositamente creati contenenti immagini del pannello CAB ridimensionabili.

Oltre ai tipi di oggetto di base, sono supportati due tipi speciali di oggetti di sovrapposizione:

* **Gli oggetti di sovrapposizione statici** sono oggetti che non accettano materiali. Sono consentite nelle vignettature 2D e 3D. Sono utili per gli accessori rimovibili in una scena di stanza, per ombre esterne dietro oggetti di sovrapposizione renderizzabili e applicazioni simili.
* **La finestra che copre gli oggetti frame** fornisce informazioni sul posizionamento per l&#39;applicazione dei file di stile per le coperture delle finestre, creati indipendentemente dalla vignettatura e che possono essere condivisi tra le vignettature.

Gli oggetti vengono raccolti in *gruppi di oggetti*, in modo analogo a un file system. Il raggruppamento è normalmente basato sulla struttura degli oggetti fisici che rappresentano (ad esempio, un gruppo &quot;Tutti gli archivi&quot; potrebbe contenere &quot;Archivi di base&quot; e &quot;Archivi murali&quot;). È consentito qualsiasi numero di livelli di gruppo. Il raggruppamento supporta l&#39;applicazione di materiali a più oggetti simili.

* [Coordinate scena](c-ir-scene-coordinates.md)
* [Risoluzione del materiale](c-ir-material-resolution.md)
