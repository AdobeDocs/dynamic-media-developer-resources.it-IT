---
description: Le variabili di sostituzione vengono utilizzate per trasferire i valori dall’URL della richiesta ai modelli di composizione memorizzati nei cataloghi delle immagini. Le variabili possono essere utilizzate anche per trasmettere lo stesso valore in punti diversi di una richiesta complessa.
seo-description: Le variabili di sostituzione vengono utilizzate per trasferire i valori dall’URL della richiesta ai modelli di composizione memorizzati nei cataloghi delle immagini. Le variabili possono essere utilizzate anche per trasmettere lo stesso valore in punti diversi di una richiesta complessa.
seo-title: Variabili di sostituzione
solution: Experience Manager
title: Variabili di sostituzione
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---


# Variabili di sostituzione{#substitution-variables}

Le variabili di sostituzione vengono utilizzate per trasferire i valori dall’URL della richiesta ai modelli di composizione memorizzati nei cataloghi delle immagini. Le variabili possono essere utilizzate anche per trasmettere lo stesso valore in punti diversi di una richiesta complessa.

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome della variabile. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore a cui impostare la variabile (stringa). </p> </td> 
 </tr> 
</table>

Le definizioni e i riferimenti delle variabili possono verificarsi nella parte query della richiesta, in `catalog::Modifier` e in `catalog::PostModifier`.

Le variabili sono definite come sopra, simili ad altri comandi IS; l&#39;interlinea &#39;$&#39; identifica il comando come definizione di variabile. Le variabili devono essere definite prima di essere utilizzate come riferimento.

Il nome della variabile *`var`* non fa distinzione tra maiuscole e minuscole e può essere costituito da una combinazione di lettere ASCII, numeri, &#39;-&#39;, &#39;_&#39; e &#39;.&#39;.

>[!NOTE]
>
>*`value`* devono essere codificati URL a passaggio singolo per una trasmissione HTTP sicura. La doppia codifica è necessaria se *`value`* viene ritrasmessa via HTTP. Ciò si verifica quando *`value`* viene sostituito in una richiesta esterna nidificata o nell&#39;attributo href di un elemento SVG `<image>`.

I riferimenti delle variabili sono costituiti dal nome della variabile delimitato da &#39;$&#39; iniziale e finale ($*var*$). I riferimenti possono verificarsi ovunque nella parte del valore di qualsiasi comando IS (ovvero tra &#39;=&#39; che segue il nome del comando e il successivo &#39;&amp;&#39; o la fine della richiesta). Le variabili personalizzate non possono essere applicate ai comandi `layer=` e `effect=`. Più variabili sono consentite nello stesso valore di comando. Il server sostituisce ogni occorrenza di ` $ *`var`*$` con *`value`*.

I riferimenti alle variabili potrebbero non essere nidificati. Tutte le occorrenze di ` $ *`var`*$` all&#39;interno di *`value`* non vengono sostituite.

Ad esempio, il frammento di richiesta:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

risolve in:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; non è un carattere riservato; può verificarsi altrimenti nella richiesta. Ad esempio, `src=my$image$file.tif` è un comando valido (supponendo che esista una voce di catalogo o un file immagine denominato `my$image$file.tif`), mentre `wid=$number$` non lo è, perché `wid` richiede un argomento numerico.

## Elaborazione delle variabili nelle richieste nidificate {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`Le `*$` differenze possono verificarsi ovunque all’interno delle parentesi graffe di una richiesta nidificata di Image Server o Image Rendering, inclusa la parte sinistra dell’icona separazione del percorso dalla query. Il server sostituisce questi riferimenti con valori (dall&#39;URL o da `catalog::Modifier` del catalogo immagini principale) prima di analizzare ed elaborare ulteriormente la richiesta nidificata.

Inoltre, tutte le definizioni ` $ *`var`*=` dell&#39;url o `catalog::Modifier` vengono inoltrate a tutte le richieste nidificate di Image Server e di Image Rendering. In questo modo tutte le definizioni delle variabili sono disponibili per tutti i modelli, indipendentemente dal livello di nidificazione.

Indipendentemente dal livello di nidificazione, ai valori variabili che devono essere sostituiti in qualsiasi punto delle richieste nidificate di rendering di immagini o Image Server o delle relative stringhe `catalog::Modifier` deve essere applicata solo la codifica HTTP a passata singola.

## Elaborazione delle variabili nelle richieste esterne incorporate {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`Le `*$` variabili che si trovano ovunque all&#39;interno delle parentesi graffe di una richiesta esterna incorporata vengono sostituite con valori di definizione variabili corrispondenti. Questo consente di inserire richieste esterne incorporate in un modello in un catalogo immagini.

I valori delle variabili che devono essere sostituiti in richieste esterne in genere devono essere codificati due volte, poiché non viene applicata alcuna codifica prima che il server tenti di trasmettere l&#39;URL esterno finale.

## Elaborazione delle variabili in file SVG {#section-a8359f9909764142b6a18ae778dca913}

` $ *`Nei file SVG possono verificarsi `*$` differenze nei valori degli attributi e nelle  `<text>` stringhe. Image Serving li sostituisce con le corrispondenti definizioni ` $ *`var`*=` note al livello di nidificazione della richiesta a cui è specificato il file SVG.

>[!NOTE]
>
>Qualsiasi valore di variabile da sostituire in un valore di attributo `href` deve essere codificato in due URL; tutti gli altri devono essere codificati singolarmente.

## Variabile di percorso predefinita {#section-930d0dd12e8f49499becc9fe8df24092}

La *`object`* specificata nel percorso della richiesta viene assegnata alla variabile predefinita `*`$object`*`. &#39; ` $ *`oggetto`*$`&#39; può essere collocato ovunque nella richiesta, nel modello a cui fa riferimento la richiesta, o in una richiesta nidificata/incorporata in cui tale oggetto è consentito, incluso il valore di `src=` e `mask=`, e il percorso di una richiesta nidificata/incorporata.

Ad esempio, la seguente richiesta riutilizzerà l’immagine specificata nel percorso come origine di un livello in una richiesta nidificata:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Equivale a

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

È possibile sostituire la definizione di `*`$object`*` specificando in modo esplicito ` $ *`object`*=` con il valore desiderato.

La variabile di percorso predefinita viene comunemente utilizzata insieme a `template=`.

## Predefinito {#section-b02483d15529444586a2e9504805b155}

Nessuno. Solo le variabili definite verranno sostituite dal server (fatta eccezione per la variabile di percorso predefinita $object, che verrà sempre sostituita). Eventuali occorrenze di ` $ *`var`*$` rimangono letterali se `*`var`*`non è possibile trovare una corrispondenza con una definizione di variabile esistente.

## Esempi {#section-fba9393df6984247b7e30b3f93992e86}

Vedere &quot;Esempio A&quot; in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
