---
description: Le vignettature sono immagini create con Dynamic Media Image Authoring per l’utilizzo con il rendering delle immagini.
solution: Experience Manager
title: Vignettature
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---


# Vignettature{#vignettes}

Le vignettature sono immagini create con Dynamic Media Image Authoring per l’utilizzo con il rendering delle immagini.

IR supporta due tipi di base di vignettatura: *2D* e *3D*. Le scene delle stanze sono in genere vignettature 3D che possono rappresentare riflessi, mentre la maggior parte delle altre scene, come abbigliamento o tappezzeria, sono in genere vignettature 2D che non hanno capacità di rendering dei riflessi.

Le vignettature contengono una *vista* e una gerarchia di *oggetti*.

La vista è il contenitore dell’immagine principale, delle mappe di illuminazione condivise, delle mappe di riflessione condivise e di altri dati associati all’intera immagine.

La gerarchia di oggetti è composta da *gruppi di oggetti*, *oggetti standard* e *oggetti sovrapposti*.

Ogni oggetto standard controlla un&#39;area dell&#39;immagine di visualizzazione, definita con una scala di grigi *mask*. Le maschere degli oggetti standard non si sovrappongono mai. Gli oggetti standard non possono essere nascosti direttamente, ma possono essere coperti parzialmente o interamente da oggetti sovrapposti. La maggior parte o tutti gli oggetti di una tipica vignettatura sono oggetti standard.

Sovrapponi il livello degli oggetti sopra l’immagine di visualizzazione e l’uno sull’altro. L&#39;ordine di sovrapposizione è definito da un valore z assegnato all&#39;oggetto. Gli oggetti di sovrapposizione sono utili quando parti di una scena devono essere visualizzate o nascoste dinamicamente.

Sono supportati diversi tipi di oggetti (standard e sovrapposizione), ciascuno dei quali ha uno scopo distinto:

* **Gli oggetti**  planari (in vignettature 3D) e gli oggetti **** piani (in vignettature 2D) accettano materiali di texture ripetibili. Sono in genere utilizzati per pavimenti, contropiani e altre superfici piane che richiedono solo la mappatura prospettica.

* **Oggetti** di linea di flussoToccate superfici curve di forma fluida come la tappezzeria e sono utilizzati occasionalmente anche per oggetti di abbigliamento. Possono essere utilizzati nelle vignettature 2D e 3D e, se completamente creati, partecipano al rendering dei riflessi.
* **Gli** oggetti non testurabili consentono solo la modifica del colore. Sono consentiti nelle vignettature 2D e 3D. Sono intrinsecamente non testurabili, oppure possono essere un oggetto planare o scorrevole con un flag speciale &#39;Nessuna texture&#39; impostato. Questa funzione è utile nelle vignettature 3D per consentire agli oggetti di partecipare al rendering del riflesso, anche se l&#39;oggetto accetta solo materiali in tinta unita.
* **Gli** oggetti di sketch vengono utilizzati in modo ottimale per gli oggetti in tessuto con pieghe e rughe, come gli articoli di abbigliamento. Come per gli oggetti con linee di flusso, possono essere utilizzati nelle vignettature 2D e 3D, anche se l&#39;applicazione nelle vignettature 3D è limitata.
* **Gli** oggetti parete sono simili agli oggetti planari e sono supportati solo nelle vignettature 3D. Hanno informazioni di layout speciali che consentono l&#39;applicazione di due diverse finiture (superiore e inferiore) e fino a tre materiali di bordo della parete. Quando viene creata correttamente, i materiali applicati alle pareti scorreranno accuratamente e senza soluzione di continuità tra le pareti adiacenti, per applicazioni realistiche di sfondo/parete. Gli oggetti parete non supportano la rotazione della texture.
* **Gli** oggetti cabinet sono consentiti solo nelle vignettature 3D. Sono utilizzati per creare armadi da cucina e da bagno con requisiti di layout complessi. Gli oggetti cabinet accettano texture ripetibili e file *stile cabinet* appositamente creati contenenti immagini ridimensionabili del pannello cabinet.

Oltre ai tipi di oggetto di base, sono supportati due tipi speciali di oggetti di sovrapposizione:

* **Gli** oggetti di sovrapposizione statici sono oggetti che non accettano materiali. Sono consentiti nelle vignettature 2D e 3D. Sono utili per gli accessori rimovibili in una scena della stanza, per le ombre esterne dietro oggetti sovrapposti e applicazioni simili.
* **Gli** oggetti frame che coprono le finestre forniscono informazioni sulla posizione per l&#39;applicazione di file di stile di coperture delle finestre, creati indipendentemente dalla vignettatura e che possono essere condivisi tra le vignettature.

Gli oggetti vengono raccolti in *gruppi di oggetti*, in modo simile a un file system. Il raggruppamento si basa normalmente sulla struttura degli oggetti fisici che rappresentano (ad esempio, un gruppo &#39;Tutti gli armadi&#39; potrebbe contenere &#39;Cabine di base&#39; e &#39;Cabine di muro&#39;). È consentito un numero qualsiasi di livelli di gruppo. Il raggruppamento supporta l&#39;applicazione di materiali a più oggetti simili.

* [Coordinate scena](c-ir-scene-coordinates.md)
* [Risoluzione del materiale](c-ir-material-resolution.md)
