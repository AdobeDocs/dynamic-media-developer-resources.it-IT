---
description: I modelli possono essere utilizzati per ridurre la lunghezza e la complessità delle richieste che compongono più livelli di immagine o che includono testo in formato rtf.
solution: Experience Manager
title: Modelli
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# Modelli{#templates}

I modelli possono essere utilizzati per ridurre la lunghezza e la complessità delle richieste che compongono più livelli di immagine o che includono testo in formato rtf.

Le variabili personalizzate possono essere utilizzate per semplificare ulteriormente l’utilizzo dei modelli. I modelli sono spesso impostati per consentire un semplice scambio di immagini o testo o per impostare altre opzioni in fase di esecuzione.

I modelli vengono memorizzati come record nei cataloghi di immagini, con il corpo del modello nel campo `catalog::Modifier` e il campo `catalog::Path` vuoto o specificando un’immagine di sfondo statica che non può essere modificata dinamicamente.

I modelli sono specificati con il comando `template=` o nel componente percorso dell’URL della richiesta. Per la maggior parte delle applicazioni si consiglia di utilizzare il comando `template=` per specificare i modelli. Il comando `template=`non deve essere presente nel campo `catalog::PostModifier` e può verificarsi solo nel campo `catalog::Modifier` in una richiesta IS nidificata (ovvero in un costrutto `src=is{...}`). È possibile che non venga fatto riferimento ai record del modello nei comandi `src=` o `mask=`.

Tutti i comandi `src=` o `mask=`incorporati nel modello possono essere risolti nel catalogo principale della richiesta o in un catalogo di immagini diverso. Se non viene specificato esplicitamente nessun `rootId`, viene utilizzato il catalogo principale. Il modello specificato con `template=` può anche trovarsi nel catalogo principale o in un catalogo di immagini diverso.

Si consiglia vivamente di includere sempre le definizioni predefinite per tutte le variabili utilizzate in un modello. In questo modo, l’output dell’immagine del modello può sempre essere visualizzato semplicemente specificando i relativi `attribute::RootId` e `catalog::Id`, senza dover sapere quali variabili vengono utilizzate nel modello.

La variabile di sostituzione del percorso predefinita `$object$` può essere utilizzata per applicare l’oggetto immagine specificato nel percorso URL a qualsiasi sorgente o maschera di livello ( `src=` o `mask=`), anche nelle richieste nidificate o incorporate.

* [Esempio A](r-example-a.md)
* [Esempio B](r-example-b.md)
* [Esempio C](r-example-c.md)
