---
description: I modelli possono essere utilizzati per ridurre la lunghezza e la complessità delle richieste che compongono più livelli di immagine o che includono testo in formato rtf.
seo-description: I modelli possono essere utilizzati per ridurre la lunghezza e la complessità delle richieste che compongono più livelli di immagine o che includono testo in formato rtf.
seo-title: Modelli
solution: Experience Manager
title: Modelli
topic: Scene7 Image Serving - Image Rendering API
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Modelli{#templates}

I modelli possono essere utilizzati per ridurre la lunghezza e la complessità delle richieste che compongono più livelli di immagine o che includono testo in formato rtf.

Le variabili personalizzate possono essere utilizzate per semplificare ulteriormente l&#39;utilizzo del modello. I modelli sono spesso configurati per consentire un facile scambio di immagini o testo o per impostare altre opzioni in fase di esecuzione.

I modelli vengono memorizzati come record nei cataloghi di immagini, con il corpo del modello nel campo `catalog::Modifier` e il campo `catalog::Path` vuoto o con la specifica di un&#39;immagine di sfondo statica che non può essere modificata in modo dinamico.

I modelli vengono specificati con il comando `template=` o nel componente percorso dell&#39;URL della richiesta. Per la maggior parte delle applicazioni si consiglia di utilizzare il comando `template=` per specificare i modelli. Il comando `template=`non deve essere presente nel campo `catalog::PostModifier` e può verificarsi solo nel campo `catalog::Modifier` in una richiesta IS nidificata (ovvero in un costrutto `src=is{...}`). I record modello non possono essere citati nei comandi `src=` o `mask=`.

Tutti i comandi `src=` o `mask=`incorporati nel modello possono essere risolti nel catalogo principale della richiesta o in un altro catalogo immagini. Se non viene specificato in modo esplicito `rootId`, viene utilizzato il catalogo principale. Il modello specificato con `template=` può anche trovarsi nel catalogo principale o in un altro catalogo immagini.

Si consiglia vivamente di includere sempre definizioni predefinite per tutte le variabili utilizzate in un modello. In questo modo, l&#39;output dell&#39;immagine del modello può sempre essere visualizzato semplicemente specificando `attribute::RootId` e `catalog::Id`, senza dover sapere quali variabili vengono utilizzate nel modello.

La variabile di sostituzione del percorso predefinita `$object$` può essere utilizzata per applicare l’oggetto immagine specificato nel percorso url a qualsiasi origine o maschera di livello ( `src=` o `mask=`), anche in richieste nidificate o incorporate.

* [Esempio A](r-example-a.md)
* [Esempio B](r-example-b.md)
* [Esempio C](r-example-c.md)
