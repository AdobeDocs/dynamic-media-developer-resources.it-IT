---
title: Modelli
description: I modelli possono essere utilizzati per ridurre la lunghezza e la complessità delle richieste che comprimono più livelli di immagine o che includono testo in formato rtf.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Modelli{#templates}

I modelli possono essere utilizzati per ridurre la lunghezza e la complessità delle richieste che comprimono più livelli di immagine o che includono testo in formato rtf.

Le variabili personalizzate possono essere utilizzate per semplificare ulteriormente l’utilizzo dei modelli. I modelli sono spesso impostati per consentire un semplice scambio di immagini o testo o per impostare altre opzioni in fase di esecuzione.

I modelli vengono memorizzati come record nei cataloghi di immagini, con il corpo del modello nel `catalog::Modifier` e `catalog::Path` campo vuoto o specifica un&#39;immagine di sfondo statica che non può essere modificata dinamicamente.

I modelli sono specificati con `template=` o nel componente percorso dell’URL della richiesta. Per la maggior parte delle applicazioni si consiglia di utilizzare il `template=` per specificare i modelli. Il `template=`il comando non deve essere presente nel `catalog::PostModifier` e può essere presente solo nel `catalog::Modifier` in una richiesta IS nidificata (ad esempio in una richiesta `src=is{...}` costrutto). Non è possibile fare riferimento ai record del modello in `src=` o `mask=`comandi.

Qualsiasi `src=` o `mask=`i comandi incorporati nel modello possono essere risolti nel catalogo principale della richiesta o in un diverso catalogo immagini. In caso negativo `rootId` viene specificato in modo esplicito, si presuppone che il catalogo principale sia. Il modello specificato con `template=` può trovarsi anche nel catalogo principale o in un altro catalogo di immagini.

Si consiglia vivamente di includere sempre le definizioni predefinite per tutte le variabili utilizzate in un modello. In questo modo, l’output dell’immagine del modello può sempre essere visualizzato specificando semplicemente i `attribute::RootId` e `catalog::Id`, senza dover sapere quali variabili vengono utilizzate nel modello.

Variabile di sostituzione percorso predefinita `$object$` può essere utilizzato per applicare l&#39;oggetto immagine specificato nel percorso url a qualsiasi sorgente o maschera di livello ( `src=` o `mask=`), anche nelle richieste nidificate o incorporate.

* [Esempio A](r-example-a.md)
* [Esempio B](r-example-b.md)
* [Esempio C](r-example-c.md)
