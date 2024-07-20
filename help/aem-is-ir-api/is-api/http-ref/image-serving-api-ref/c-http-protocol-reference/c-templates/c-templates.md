---
title: Modelli
description: I modelli possono essere utilizzati per ridurre la lunghezza e la complessità delle richieste che comprimono più livelli di immagine o che includono testo in formato rtf.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Modelli{#templates}

I modelli possono essere utilizzati per ridurre la lunghezza e la complessità delle richieste che comprimono più livelli di immagine o che includono testo in formato rtf.

Le variabili personalizzate possono essere utilizzate per semplificare ulteriormente l’utilizzo dei modelli. I modelli sono spesso impostati per consentire un semplice scambio di immagini o testo o per impostare altre opzioni in fase di esecuzione.

I modelli vengono archiviati come record nei cataloghi di immagini, con il corpo del modello nel campo `catalog::Modifier` e il campo `catalog::Path` vuoto oppure specificando un&#39;immagine di sfondo statica che non può essere modificata dinamicamente.

I modelli sono specificati con il comando `template=` o nel componente percorso dell&#39;URL della richiesta. Per la maggior parte delle applicazioni si consiglia di utilizzare il comando `template=` per specificare i modelli. Il comando `template=` non deve essere presente nel campo `catalog::PostModifier` e può essere presente solo nel campo `catalog::Modifier` in una richiesta IS nidificata, ovvero in un costrutto `src=is{...}`. Non è possibile fare riferimento ai record modello nei comandi `src=` o `mask=`.

Tutti i comandi `src=` o `mask=` incorporati nel modello possono essere risolti nel catalogo principale della richiesta o in un altro catalogo immagini. Se non viene specificato in modo esplicito alcun `rootId`, viene utilizzato il catalogo principale. Il modello specificato con `template=` può trovarsi anche nel catalogo principale o in un altro catalogo immagini.

Si consiglia vivamente di includere sempre le definizioni predefinite per tutte le variabili utilizzate in un modello. In questo modo, l&#39;output dell&#39;immagine del modello può sempre essere visualizzato specificando i relativi `attribute::RootId` e `catalog::Id`, senza dover sapere quali variabili vengono utilizzate nel modello.

La variabile di sostituzione percorso predefinita `$object$` può essere utilizzata per applicare l&#39;oggetto immagine specificato nel percorso URL a qualsiasi origine o maschera di livello ( `src=` o `mask=`), anche nelle richieste nidificate o incorporate.

* [Esempio A](r-example-a.md)
* [Esempio B](r-example-b.md)
* [Esempio C](r-example-c.md)
